# Flipturn

Flipturn is an EV charging management platform for businesses and fleet
operators — charger monitoring, energy management, fleet charging, access
control, and payments/billing — sitting on top of OCPP 1.6/2.0.1 chargers (with
OCPI for roaming partners). Backed by Accel and CRV.

- Website: https://www.getflipturn.com
- API docs: https://api-docs.getflipturn.com/ (base URL `https://api.getflipturn.com/api`)
- Status: https://status.getflipturn.com/
- Security/compliance: https://www.getflipturn.com/product/security (SOC 2, GDPR)

## Artifacts

This profile was enriched by the API Evangelist pipeline. The Flipturn API
publishes no OpenAPI, so the spec here is generated from the public GitBook docs
(`llms.txt` + markdown pages). Captured artifacts:

- `openapi/` — OpenAPI 3.1 generated from the docs (26 operations across 13 resources)
- `overlays/` — API Evangelist enhancements overlay
- `authentication/` — bearer API-key auth profile
- `conventions/` — pagination, rate limiting, error envelope, versioning
- `errors/` — error/response-code catalog
- `rate-limits/` — 200 req/min per key
- `data-model/` — entity-relationship graph
- `conformance/` — OCPP/OCPI/auth/pagination + SOC 2/GDPR
- `mcp/` — candidate MCP tool list (one per operation)
- `skills/` — agent skills (export sessions, sync fleet access IDs, monitor health)
- `agentic-access/` — recommended x-agentic-access contracts
- `lifecycle/` — versioning + status page
- `security/` — domain-security probe + trust center
- `llms/` — verbatim `llms.txt`
