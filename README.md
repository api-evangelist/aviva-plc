# Aviva plc (aviva-plc)

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

Aviva plc is the United Kingdom's largest insurer and one of the ten biggest insurance groups in Europe, listed on the London Stock Exchange and serving roughly 20 million UK customers across the UK, Ireland and Canada following completion of its acquisition of Direct Line Insurance Group on 1 July 2025. Aviva is a composite carrier: UK and Ireland general insurance (personal and commercial motor, property and liability), the UK's largest life insurance book, a growing corporate and individual health business, workplace pensions and wealth, and Aviva Investors as the asset-management arm. Aviva Canada is that market's second-largest property and casualty insurer.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/aviva-plc/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/aviva-plc/refs/heads/main/apis.yml)

## API Posture

Aviva runs a real API programme that is **not publicly consumable**. A first-party developer portal exists at [developer.aviva.co.uk](https://developer.aviva.co.uk/), served under an Extended Validation certificate issued to Aviva PLC and built on Kong Konnect. Its own unauthenticated metadata endpoint (`GET /api/v2/portal`, HTTP 200) reports `is_public: false`, `rbac_enabled: true` and `oidc_auth_enabled: true`. Every content path — `/documentation`, `/developer-guide`, `/health`, `/api-details/*` — returns **HTTP 403**, and both public sitemaps (`/__sitemap__/pages.xml`, `/__sitemap__/apis.xml`) are empty. It is a partner login wall, not a self-serve developer portal.

Behind the wall sits Aviva's Health API family — Private Medical Insurance pricing (quote/rating) and purchase/enrolment (bind/issue) for consumer and SME. Partners apply for sandbox access and apply again for production consumption. **No OpenAPI, Swagger, AsyncAPI, GraphQL SDL, `.proto` or official Postman workspace is published**, so no specification could be harvested. There is no documented FNOL API.

The larger integration channel is not the portal at all. In the UK, Aviva trades with brokers through **Polaris UK's imarket** — Aviva is a named participating insurer — over Polaris code lists and PL EDI messages, reaching Acturis, Applied Systems, Bravo Digital Trader, Open GI and SSP. In December 2024 Aviva and Acturis launched what both describe as the first insurer claims API integrated into Acturis: a **one-way** push of new and updated motor, property and liability claim records into a broker's Acturis system.

**ACORD posture:** no ACORD reference found. No ACORD, AL3, ACORD XML, ACORD-certified or NGDS mention appears on any Aviva surface. That is the expected UK pattern — the UK carrier-to-broker standard is Polaris, not ACORD; ACORD reaches the UK mainly through Lloyd's Blueprint Two (EBOT/ECOT on ACORD 2016-10), a London Market programme Aviva's UK retail and commercial business does not trade through.

## Tags

- Insurance
- United Kingdom
- Property and Casualty
- Life Insurance
- Health Insurance
- Claims
- Underwriting
- Broker
- Workplace Pensions
- Carrier

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

Recorded from the developer portal's own indexed service-catalogue page titles. Both are partner-gated and returned HTTP 403 to unauthenticated requests; no base URL or specification is published.

### Aviva Private Medical Insurance Consumer Pricing API

Calculates premiums for Aviva consumer Private Medical Insurance policies — the quote/rating verb of the Aviva Health API family.

- **Human URL:** [https://developer.aviva.co.uk/api-details/details-pricing](https://developer.aviva.co.uk/api-details/details-pricing)

#### Properties

- [Developer Portal](https://developer.aviva.co.uk/)
- [Documentation](https://developer.aviva.co.uk/documentation)

### Aviva Private Medical Insurance Consumer Purchase API

Submits applications for PMI policy enrolment into Aviva systems, automating the quote-to-buy journey — the bind/issue verbs of the Aviva Health API family.

- **Human URL:** [https://developer.aviva.co.uk/api-details/details-purchase](https://developer.aviva.co.uk/api-details/details-purchase)

#### Properties

- [Developer Portal](https://developer.aviva.co.uk/)
- [Documentation](https://developer.aviva.co.uk/documentation)

## Links

- [Website](https://www.aviva.com/)
- [Aviva UK](https://www.aviva.co.uk/)
- [Developer Portal](https://developer.aviva.co.uk/) — partner-gated
- [Aviva Broker Connect (B2B)](https://connect.avivab2b.co.uk/)
- [Newsroom](https://www.aviva.com/newsroom/)
- [LinkedIn](https://www.linkedin.com/company/aviva-plc)
