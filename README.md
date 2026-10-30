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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Flipturn is an EV charging management platform that gives businesses and fleet operators one system to monitor chargers, manage energy costs, run fleet charging operations, control access, and handle payments and billing. Its software layer sits on top of OCPP 1.6 and 2.0.1 chargers (with OCPI support for roaming partners) and serves delivery fleets, transit agencies, multifamily housing, dealerships, workplaces, hospitality, retail, parking, and valet. Flipturn also publishes a JSON REST API, secured with a bearer API key, that exposes sites, chargers and ports, charging sessions, charger health and uptime, access IDs (RFID cards and vehicles), vehicles, alerts, charger errors, raw OCPP messages, port reservations, site power limits, vehicle departure times, and maintenance windows — designed for integrating charging data with ticketing platforms, data warehouses, and transportation management systems. Flipturn is backed by Accel and CRV.

**Areas:** Company · EV Charging · Electric Vehicles · Fleet Management · Energy · Charging Infrastructure · OCPP · OCPI · Mobility · REST API

## Flipturn on APIs.io

Everything profiled for Flipturn is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/flipturn/](https://apis.io/providers/flipturn/)** — or go straight to one of the APIs or properties below.

### APIs (13)

- [Flipturn Access IDs API](https://apis.io/apis/flipturn/flipturn-access-ids-api/) — RFID cards and vehicle MAC IDs used to authorize charging.
- [Flipturn Alerts API](https://apis.io/apis/flipturn/flipturn-alerts-api/) — Alerts raised by the platform.
- [Flipturn Charger Health API](https://apis.io/apis/flipturn/flipturn-charger-health-api/) — Uptime, error, and utilization statistics.
- [Flipturn Chargers API](https://apis.io/apis/flipturn/flipturn-chargers-api/) — Individual charger detail lookups.
- [Flipturn Charging Sessions API](https://apis.io/apis/flipturn/flipturn-charging-sessions-api/) — Historical and in-progress charging sessions.
- [Flipturn Departure Times API](https://apis.io/apis/flipturn/flipturn-departure-times-api/) — Scheduled vehicle departure times synced from a TMS.
- [Flipturn Errors API](https://apis.io/apis/flipturn/flipturn-errors-api/) — Charger error records.
- [Flipturn Maintenance Windows API](https://apis.io/apis/flipturn/flipturn-maintenance-windows-api/) — Scheduled maintenance windows for chargers.
- [Flipturn OCPP Messages API](https://apis.io/apis/flipturn/flipturn-ocpp-messages-api/) — Raw OCPP protocol messages for a charger.
- [Flipturn Reservations API](https://apis.io/apis/flipturn/flipturn-reservations-api/) — OCPP ReserveNow / CancelReservation port reservations.
- [Flipturn Site Power Limits API](https://apis.io/apis/flipturn/flipturn-site-power-limits-api/) — Cost and capacity power limits for a site.
- [Flipturn Sites API](https://apis.io/apis/flipturn/flipturn-sites-api/) — Sites, their chargers and ports, and current status.
- [Flipturn Vehicles API](https://apis.io/apis/flipturn/flipturn-vehicles-api/) — Electric vehicles and their associated access IDs.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [flipturn](https://apis.io/servers/flipturn/flipturn/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Flipturn Agentic Access](https://apis.io/agentic-access/flipturn/flipturn-agentic-access/)

#### Collections (13)

Postman and Open Collection request collections.

- [Flipturn Access IDs API](https://apis.io/collections/flipturn/open-flipturn-access-ids-api/)
- [Flipturn Access IDs Alerts API](https://apis.io/collections/flipturn/open-flipturn-alerts-api/)
- [Flipturn Access IDs Charger Health API](https://apis.io/collections/flipturn/open-flipturn-charger-health-api/)
- [Flipturn Access IDs Chargers API](https://apis.io/collections/flipturn/open-flipturn-chargers-api/)
- [Flipturn Access IDs Charging Sessions API](https://apis.io/collections/flipturn/open-flipturn-charging-sessions-api/)
- [Flipturn Access IDs Departure Times API](https://apis.io/collections/flipturn/open-flipturn-departure-times-api/)
- [Flipturn Access IDs Errors API](https://apis.io/collections/flipturn/open-flipturn-errors-api/)
- [Flipturn Access IDs Maintenance Windows API](https://apis.io/collections/flipturn/open-flipturn-maintenance-windows-api/)
- [Flipturn Access IDs OCPP Messages API](https://apis.io/collections/flipturn/open-flipturn-ocpp-messages-api/)
- [Flipturn Access IDs Reservations API](https://apis.io/collections/flipturn/open-flipturn-reservations-api/)
- [Flipturn Access IDs Site Power Limits API](https://apis.io/collections/flipturn/open-flipturn-site-power-limits-api/)
- [Flipturn Access IDs Sites API](https://apis.io/collections/flipturn/open-flipturn-sites-api/)
- [Flipturn Access IDs Vehicles API](https://apis.io/collections/flipturn/open-flipturn-vehicles-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Flipturn Openapi Overlay](https://apis.io/overlays/flipturn/flipturn-openapi-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Flipturn Authentication](https://apis.io/security/flipturn/flipturn-authentication/)
- [Flipturn Domain Security](https://apis.io/security/flipturn/flipturn-domain-security/)
- [Flipturn Trust Center](https://apis.io/security/flipturn/flipturn-trust-center/)

#### Rate limits (1)

Published request limits.

- [Flipturn Rate Limits](https://apis.io/rate-limits/flipturn/flipturn-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](http://www.getflipturn.com)
- [Documentation](https://api-docs.getflipturn.com/)
- [Getting started](https://api-docs.getflipturn.com/authorization.md)
- [API reference](https://api-docs.getflipturn.com/)
- [Sign up](https://www.getflipturn.com/getdemo)
- [Support](https://www.getflipturn.com/contact-us)
- [Blog](https://www.getflipturn.com/blog)
- [Compliance](https://www.getflipturn.com/product/security)
- [Terms of service](https://www.getflipturn.com/terms-of-service)
- [Privacy policy](https://www.getflipturn.com/privacy-policy)
- [Status](https://status.getflipturn.com/)

## API Evangelist rating

**Kin Score 46.8** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 14.6 |
| Contract governance | 18.2 |
| Operational transparency | 36.8 |
| Developer ergonomics | 58.9 |
| Access clarity | 50.0 |

**Agent readiness 26.0** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 24.6** — Energy & Utilities

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/flipturn/](https://apis.io/providers/flipturn/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Flipturn: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/flipturn/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
