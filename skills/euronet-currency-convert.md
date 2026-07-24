---
name: Convert currency with Xe Currency Data
description: Look up supported currencies and convert an amount between currencies (live or historic) using the Xe Currency Data API.
api: openapi/xe-currency-data-api-openapi.json
operations:
  - "GET /currencies"
  - "GET /convert_from"
  - "GET /convert_to"
  - "GET /historic_rate"
  - "GET /account_info"
---

# Convert currency with the Xe Currency Data API

Base URL: `https://xecdapi.xe.com/v1`

## Auth
HTTP Basic. Username = your Xe account id, password = your API key (`basicAuth`).
Get one via the 7-day free trial at https://xecd.xe.com/account/signup.php?freetrial.

## Steps
1. (Optional) Check your plan/usage with `GET /account_info`.
2. Confirm the currency codes you need with `GET /currencies`.
3. For a live conversion, call `GET /convert_from` with query params:
   - `from` (ISO 4217 source code), `to` (one or more target codes), `amount`.
   - Optional: `inverse`, `decimal_places`, `margin`, `obsolete`.
   Use `GET /convert_to` to invert the direction.
4. For a rate on a specific date, call `GET /historic_rate` (single date) or
   `GET /historic_rate/period` (date range).

## Rules
- Each rate returned counts as one request against your monthly package quota
  (Medium = 100,000/month). Watch `X-RateRequest-Remaining` / `X-RateLimit-Remaining`;
  a `429` means the quota is exhausted — back off until `X-RateRequest-Reset`.
- Errors return `{ code, message, documentationUrl }`. Read `documentationUrl` for detail.
- Rates are mid-market; apply your own margin via the `margin` param if needed.
