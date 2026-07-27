---
name: Monitor Flipturn charger health, errors, and alerts
description: Pull uptime/utilization statistics, recent charger errors, and alerts to build a reliability report for a charging estate.
api: openapi/flipturn-openapi.yml
operations: [getChargerHealth, listErrors, listAlerts, listSites]
---

# Monitor Flipturn charger health

Build reliability and uptime reporting for a charging estate.

## Auth
`Authorization: Bearer {api_key}`. Base URL `https://api.getflipturn.com/api`.

## Steps

1. **(Optional) Scope** — call `listSites` (`GET /sites`) for site/charger IDs.
2. **Health stats** — call `getChargerHealth` (`GET /charger-health`) with an
   optional `startTimestamp`/`endTimestamp` (defaults to the last 30 days) and
   optional `siteIds`/`chargerIds`. Read `summary` for aggregates and `data[]`
   for per-charger/per-port uptime, error, and utilization stats. This endpoint
   enforces stricter rate limits — call it sparingly.
3. **Recent errors** — call `listErrors` (`GET /errors`) with `afterTimestamp`
   to pull charger error rows (reverse chronological, up to 2000/page). Each row
   carries `ocppErrorCode`, `ocppStatus`, and `errorCategory`
   (`endedCharging`/`preventedCharging`/`muted`/`other`).
4. **Alerts** — call `listAlerts` (`GET /alerts`) with `startTimestampAfter` to
   pull alerts (`lowBattery`, `chargingCompleted`, `chargingSessionError`,
   `offlineCharger`, `lateCharging`). Set `includeMuted=true` to include muted
   ones.
5. **Paginate** — follow `pagination.nextPageCursor` until `hasNextPage` is false.

## Conventions & errors
- Cursor pagination, 200 req/min rate limit — see
  `conventions/flipturn-conventions.yml` and `rate-limits/`.
- Errors are `{ "error": string }` — see `errors/flipturn-problem-types.yml`.
