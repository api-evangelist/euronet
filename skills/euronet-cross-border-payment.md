---
name: Send a cross-border payment with Xe Payments
description: Quote, add a recipient, and book a cross-border payment on the Xe Payments API.
api: openapi/xe-payments-api-openapi.json
operations:
  - "GET /permissions"
  - "GET /tradeablecurrencies"
  - "GET /purposesofpayment/{currency}"
  - "POST /quotes"
  - "GET /recipients/fields/{country}/{currency}"
  - "POST /recipients"
  - "POST /transactions"
  - "GET /transactions/{transactionId}"
---

# Send a cross-border payment with the Xe Payments API

Production host: `payments-api.xe.com` (partner-onboarded; a sandbox environment is
available for integration testing). Auth is provisioned during partner onboarding
(not declared in the public SwaggerHub definition).

## Steps
1. Confirm entitlements with `GET /permissions`.
2. List sendable currencies with `GET /tradeablecurrencies` and valid reasons with
   `GET /purposesofpayment/{currency}`.
3. Create an FX quote with `POST /quotes`. The response wrapper carries
   `content` plus `message`/`errors`/`warnings`/`information` — inspect `errors[]`
   before proceeding even on a `200`.
4. Determine the recipient schema for the destination with
   `GET /recipients/fields/{country}/{currency}`, then create the recipient with
   `POST /recipients`.
5. Book the payment with `POST /transactions`, referencing the quote id and
   recipient id.
6. Poll `GET /transactions/{transactionId}` for settlement status.

## Rules
- `POST /transactions` executes a real money movement. There is **no documented
  idempotency-key** — do not blindly retry a booking; re-check transaction state
  with `GET /transactions/{transactionId}` before resubmitting.
- Quotes expire; refresh with `GET /quotes/{quoteId}` if stale before booking.
- Transaction/recipient listings paginate with `pageNumber` / `pageSize`.
- Errors surface inside the response wrapper's `errors[]` (`{ code, data }`), not
  always as HTTP 4xx.
