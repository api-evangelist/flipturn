---
name: Export Flipturn charging sessions to a data warehouse
description: Backfill all historical charging sessions and then poll for new ones, deduplicating by session id, using the Flipturn API.
api: openapi/flipturn-openapi.yml
operations: [listSites, listChargingSessions]
---

# Export Flipturn charging sessions

Continuously import Flipturn charging sessions into an external system (data
warehouse, BI, billing) without missing or double-inserting any.

## Auth
Send `Authorization: Bearer {api_key}` on every request. Keys are created in
cloud.getflipturn.com (Manage > API Keys) by an Owner and may be scoped to
specific sites/chargers. Base URL: `https://api.getflipturn.com/api`.

## Steps

1. **(Optional) Resolve scope** — call `listSites` (`GET /sites`) to get site and
   charger IDs if you want to filter with `siteIds`/`chargerIds`.
2. **Backfill** — call `listChargingSessions` (`GET /charging-sessions`) with **no
   time filters**. Read `data[]`, persist each session using its `id` as the
   unique key.
3. **Paginate** — if `pagination.hasNextPage` is true, repeat the call passing
   `nextPageCursor` from the previous response and keeping all other params
   identical. Stop when `hasNextPage` is false.
4. **Poll for new sessions** — on a schedule, call `listChargingSessions` with
   `endTimeAfter` set to the latest `endTime` you have seen (or a timestamp
   slightly older than your poll interval to absorb clock skew).
5. **Deduplicate** — upsert on session `id`; never rely on timestamps alone.

## Options
- `includeIntervals=true` adds 15-minute interval stats and max demand, but
  limits the key to **1 concurrent request**.
- `includeTouEnergy=true` adds time-of-use energy buckets.
- `includeInProgressSessions=true` returns in-progress sessions (nullable end
  fields).

## Conventions & errors
- Cursor pagination — see `conventions/flipturn-conventions.yml`.
- Rate limit 200 req/min per key; `429` on overage — see `rate-limits/`.
- Errors are `{ "error": string }` with HTTP 400/401/404/429 — see
  `errors/flipturn-problem-types.yml`.
