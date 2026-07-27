---
name: Sync a fleet of vehicles and RFID cards into Flipturn
description: Bulk-upsert up to 1000 access IDs (RFID cards and vehicle MAC IDs) to keep a fleet authorization list in sync with Flipturn.
api: openapi/flipturn-openapi.yml
operations: [batchUpsertAccessIds, listAccessIds, listVehicles]
---

# Sync a fleet of access IDs into Flipturn

Keep Flipturn's authorization list in sync with your fleet/vehicle management
system.

## Auth
`Authorization: Bearer {api_key}`. Base URL `https://api.getflipturn.com/api`.

## Steps

1. **Build the batch** — assemble up to **1000** items. Each item needs
   `ocppIdTag`, `name`, and `type` (`RFID` or `Vehicle`). For vehicles you may
   include a `vehicle` object (`make`/`model`/`vin`) and a `customer` name.
2. **Upsert** — call `batchUpsertAccessIds` (`PUT /access-ids/batch`). Existing
   access IDs are matched by `ocppIdTag` (updated); unmatched ones are created.
   Vehicles are matched by case-insensitive `name`; a new vehicle is created if
   none exists. Items **not** included are never deleted.
3. **Read results** — each `results[]` entry has `outcome` of `created`,
   `updated`, or `error` (with an `error` message). Other items still process
   when one fails.
4. **Verify** — call `listVehicles` (`GET /vehicles`) or `listAccessIds`
   (`GET /access-ids`) to confirm state; both are cursor-paginated.

## Idempotency
There is no idempotency-key header, but this endpoint is idempotent by design:
re-posting the same payload converges to the same state (matched by `ocppIdTag`
/ vehicle `name`). See `conventions/flipturn-conventions.yml`.

## Errors
`{ "error": string }` with HTTP 400/401 — see `errors/flipturn-problem-types.yml`.
Rate limit 200 req/min — see `rate-limits/`.
