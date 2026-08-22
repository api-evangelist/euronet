# Euronet Worldwide (euronet)

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

Euronet Worldwide (NASDAQ: EEFT) is a US-based (Leawood, Kansas) global payments and financial technology company operating across three segments: Payments Infrastructure (EFT/ATM networks, transaction processing, merchant acquiring, and the REN payments software from Euronet Software Solutions); epay (prepaid and digital-media distribution); and Money Transfer, home to its Ria, Xe, and Dandelion brands. The company processes roughly 20 billion transactions a year across 200 countries and territories.

Consistent with the fragmented US payments market (no single mandate or unified scheme API), Euronet does not publish one platform API. Its developer surface is distributed across brands — most API-natively through **Xe** (five published Swagger definitions) and **Dandelion** (a real-time, ISO 20022-compliant cross-border payments developer portal).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/euronet/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/euronet/refs/heads/main/apis.yml)

## Tags

- Payments
- United States
- Payment Processing
- Cross-Border
- Money Transfer
- Currency Exchange
- FX
- Payouts
- Real-Time Payments
- ISO 20022
- Acquiring

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Xe Currency Data API

REST JSON API serving real-time and historical exchange rates for 170+ currencies from 100+ global sources. HTTP Basic auth; 7-day free-trial self-serve signup.

- **Human URL:** [https://xecdapi.xe.com/docs/v1/](https://xecdapi.xe.com/docs/v1/)
- **Base URL:** `https://xecdapi.xe.com/v1`
- **Properties:** [OpenAPI](openapi/xe-currency-data-api-openapi.json) · [Documentation](https://xecdapi.xe.com/docs/v1/) · [API Reference](https://app.swaggerhub.com/apis/XE.com/xecdapi/1.0.2) · [Sign Up](https://xecd.xe.com/account/signup.php?freetrial)

### Xe Payments API

Cross-border payment execution — quotes, recipients, tradeable currencies, purposes of payment, and transactions for sending to 200+ countries, with a sandbox for integration testing.

- **Human URL:** [https://www.xe.com/platform/payments-api/](https://www.xe.com/platform/payments-api/)
- **Properties:** [OpenAPI](openapi/xe-payments-api-openapi.json) · [Documentation](https://www.xe.com/platform/payments-api/) · [API Reference](https://app.swaggerhub.com/apis/XE.com/xe-api_payments/1.3.0)

### Xe Mass Payments API

Batch/bulk cross-border payouts — account, quote, invoice, payments, transaction, terms, and permissions resources for high-volume disbursement.

- **Human URL:** [https://www.xe.com/platform/payments-api/](https://www.xe.com/platform/payments-api/)
- **Properties:** [OpenAPI](openapi/xe-mass-payments-api-openapi.json) · [API Reference](https://app.swaggerhub.com/apis/XE.com/xe-api_mass_payments/0.4.1)

### Xe Currency Data Tradable Rates API

Tradable (dealable) FX rates companion to the Currency Data API. The published definition ships with a SwaggerHub mock host.

- **Human URL:** [https://app.swaggerhub.com/apis/XE.com/xecdapi-tradable/1.0.0](https://app.swaggerhub.com/apis/XE.com/xecdapi-tradable/1.0.0)
- **Properties:** [OpenAPI](openapi/xe-currency-data-tradable-rates-api-openapi.json)

### XETA API

A Swagger 2.0 definition published by XE.com on SwaggerHub (16 operations). Declares host `xeta-api.xe.com/v1` (not publicly reachable at review time).

- **Human URL:** [https://app.swaggerhub.com/apis/XE.com/xeta/v1.0.0](https://app.swaggerhub.com/apis/XE.com/xeta/v1.0.0)
- **Properties:** [OpenAPI](openapi/xeta-api-openapi.json)

### Dandelion Cross-Border Payments API

Real-time, ISO 20022-compliant cross-border payments network reaching 190+ countries, ~6 billion accounts/wallets, and 550,000+ cash pickup locations. Powers payout orders (bank deposit, mobile wallet, cash pickup) and underpins Ria and Xe. Developer portal is live but the API console is login-gated, so no downloadable OpenAPI was available.

- **Human URL:** [https://public.dandelionpayments.com/](https://public.dandelionpayments.com/)
- **Properties:** [Developer Portal](https://public.dandelionpayments.com/) · [Documentation](https://www.euronet.com/products-and-solutions/dandelion/) · [Help Center](https://help.dandelionpayments.com/hc/en-gb)

## Common Properties

- [Website](https://www.euronet.com/)
- [Developer Portal](https://public.dandelionpayments.com/)
- [Documentation](https://xecdapi.xe.com/docs/v1/)
- [Help Center](https://help.dandelionpayments.com/hc/en-gb)
- [Sign Up](https://xecd.xe.com/account/signup.php?freetrial)
- [Privacy Policy](https://www.euronet.com/legal-privacy-statement/)
- [LinkedIn](https://www.linkedin.com/company/euronet-worldwide)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
