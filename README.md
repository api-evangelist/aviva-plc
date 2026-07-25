# Aviva plc (aviva-plc)

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
