# CargoWise

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

CargoWise is WiseTech Global's logistics execution platform - a single-database ERP for international freight forwarding, customs, warehousing, transport, and landside logistics. Its integration surface is delivered primarily through eAdaptor, which pairs a RESTful XML inbound service (push, query, add, and update records) with a SOAP-based outbound service (a webhook equivalent that emits messages on milestones). Payloads use CargoWise's Universal XML schemas - Universal Shipment (XUS), Universal Event (XUE), and Universal Transaction - or the legacy Native XML format. Newer REST integration (eAdaptor Next / xHub) adds OAuth 2.0 authorization-code access. The integration API is real but heavily gated - the eAdaptor Developers Guide and endpoint details are released only after a customer purchases the eAdaptor modules, and partner access runs through WiseTech accreditation and certification. Endpoints below are modeled from public developer references; the authoritative specification is not publicly published.

**Areas:** Logistics · Freight Forwarding · Supply Chain · Customs · Shipping · eAdaptor · Universal XML · EDI · WiseTech Global

## CargoWise on APIs.io

Everything profiled for CargoWise is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cargowise/](https://apis.io/providers/cargowise/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [CargoWise eAdaptor Inbound API](https://apis.io/apis/cargowise/cargowise-eadaptor-inbound-api/) — The eAdaptor Inbound Service is a RESTful XML interface for pushing data into a CargoWise (CW1) instance and querying records. A single inbound endpoint…
- [CargoWise eAdaptor Outbound API](https://apis.io/apis/cargowise/cargowise-eadaptor-outbound-api/) — The eAdaptor Outbound Service is the webhook equivalent - CargoWise emits messages to a listening SOAP service when configured Workflow Template milestones…
- [CargoWise Universal Shipment API](https://apis.io/apis/cargowise/cargowise-universal-shipment-api/) — The Universal Shipment (XUS) message is CargoWise's canonical XML model for a full logistics record - forwarding shipment, customs declaration, warehouse…
- [CargoWise Universal Event API](https://apis.io/apis/cargowise/cargowise-universal-event-api/) — The Universal Event (XUE) message carries a minimal record identifier plus the event or milestone responsible for a notification - the basis for tracking…
- [CargoWise REST Integration API](https://apis.io/apis/cargowise/cargowise-rest-integration-api/) — WiseTech's newer integration path (referred to as eAdaptor Next and xHub) adds REST access authenticated with OAuth 2.0 authorization-code flow, where a…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Cargowise Authentication](https://apis.io/security/cargowise/cargowise-authentication/)
- [Cargowise Domain Security](https://apis.io/security/cargowise/cargowise-domain-security/)
- [Cargowise Vulnerability Disclosure](https://apis.io/security/cargowise/cargowise-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cargowise Plans Pricing](https://apis.io/plans/cargowise/cargowise-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cargowise Rate Limits](https://apis.io/rate-limits/cargowise/cargowise-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cargowise.com/)
- [Documentation](https://wisetechacademy.com/explore/product-learning/)
- [Pricing](https://www.cargowise.com/cargowise-value-pack/)
- [Support](https://www.cargowise.com/support/)
- [Blog](https://www.cargowise.com/news/)
- [Terms of service](https://www.wisetechglobal.com/legal/terms-of-use/)
- [Privacy policy](https://www.wisetechglobal.com/legal/privacy-and-data-protection-notice/)
- [GitHub](https://github.com/WiseTechGlobal)

## API Evangelist rating

**Kin Score 30.4** — thin · rubric 0.24.0 · scored 2026-10-20

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 15.8 |
| Developer ergonomics | 28.6 |
| Access clarity | 73.2 |

**Agent readiness 16.4** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 25.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cargowise/](https://apis.io/providers/cargowise/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for CargoWise: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cargowise/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
