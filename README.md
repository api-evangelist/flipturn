# Flipturn

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
