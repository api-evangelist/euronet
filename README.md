# Euronet Worldwide (euronet)

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
