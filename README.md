# Aviva

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

Aviva plc is the United Kingdom's largest insurer and one of the ten biggest insurance groups in Europe, listed on the London Stock Exchange and serving roughly 20 million UK customers across the UK, Ireland and Canada following completion of its acquisition of Direct Line Insurance Group on 1 July 2025. Aviva is a composite carrier rather than a single-line one: UK and Ireland general insurance (personal and commercial motor, property and liability), the UK's largest life insurance book, a growing corporate and individual health business, workplace pensions and wealth, and Aviva Investors as the asset-management arm. Aviva Canada is that market's second-largest property and casualty insurer. Aviva's API posture is that of a carrier, not a platform. It operates a real, modern developer portal at developer.aviva.co.uk — a Kong Konnect portal fronted by Aviva's own EV certificate — but the portal reports is_public false with RBAC and OIDC authentication enabled, and every content path returns HTTP 403 to an unauthenticated request. It is explicitly a partner surface: the portal's own copy describes Partners discovering, accessing and consuming Aviva Health APIs, with sandbox access granted on application and production consumption granted on approval. There is no self-serve signup, no public API reference, no downloadable OpenAPI, no public Postman workspace, no GraphQL surface and no published event catalogue. The far larger integration channel is not the portal at all: in the UK, Aviva trades with brokers through Polaris UK's imarket and its PL EDI message and code-list standards, reaching broker systems such as Acturis, Applied Systems, Open GI, Bravo and SSP, and in December 2024 Aviva became the first insurer to launch a claims API integrated directly into Acturis, pushing new and updated motor, property and liability claim records into brokers' management systems. No ACORD reference was found on any Aviva surface; the UK's standards seam here is Polaris, not ACORD. This record is therefore an honest stub: a real but partner-gated API programme with no public self-serve surface to harvest.

**Areas:** Insurance · United Kingdom · Property and Casualty · Life Insurance · Health Insurance · Claims · Underwriting · Workplace Pensions · Carrier

## Aviva on APIs.io

Everything profiled for Aviva is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/aviva-plc/](https://apis.io/providers/aviva-plc/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [Aviva Private Medical Insurance Consumer Pricing API](https://apis.io/apis/aviva-plc/aviva-private-medical-insurance-consumer-pricing-api/) — Listed in the Aviva API Developer Portal service catalogue as an API that calculates premiums for Aviva consumer Private Medical Insurance policies — the…
- [Aviva Private Medical Insurance Consumer Purchase API](https://apis.io/apis/aviva-plc/aviva-private-medical-insurance-consumer-purchase-api/) — Listed in the Aviva API Developer Portal service catalogue as the purchase counterpart to the pricing API, enabling partners to submit applications for PMI…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Aviva Plc Authentication](https://apis.io/security/aviva-plc/aviva-plc-authentication/)
- [Aviva Plc Domain Security](https://apis.io/security/aviva-plc/aviva-plc-domain-security/)

#### Rate limits (1)

Published request limits.

- [Aviva Plc Rate Limits](https://apis.io/rate-limits/aviva-plc/aviva-plc-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.aviva.com/)
- [Documentation](https://developer.aviva.co.uk/documentation)
- [Getting started](https://developer.aviva.co.uk/get-started)
- [Support](https://developer.aviva.co.uk/contact)
- [Blog](https://www.aviva.com/newsroom/)
- [Terms of service](https://www.aviva.com/legal/)
- [Privacy policy](https://www.aviva.com/privacy-policy/)

## API Evangelist rating

**Kin Score 24.2** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 0.0 |
| Contract governance | 18.2 |
| Operational transparency | 21.1 |
| Developer ergonomics | 39.3 |
| Access clarity | 21.1 |

**Agent readiness 13.3** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
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

**Regulatory alignment 21.9** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/aviva-plc/](https://apis.io/providers/aviva-plc/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Aviva: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/aviva-plc/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
