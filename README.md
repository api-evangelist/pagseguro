# PagSeguro / PagBank (pagseguro)

PagSeguro (operating consumer-facing as **PagBank**) is one of Brazil's largest payment processors and digital-banking platforms. Originally spun out of UOL (Universo Online) and listed on the NYSE under **PAGS**, the company offers an end-to-end financial stack: online payments, in-person card acceptance through the Moderninha and Minizinha terminal families, Pix instant payments, boleto bancário, credit and debit cards, recurring subscriptions, marketplace split, payouts, account-as-a-service, and a digital bank with cards, credit, and investments.

The developer portal at [developer.pagbank.com.br](https://developer.pagbank.com.br/) exposes a REST API surface — Orders, Charges, Public Keys, Checkout, Recurring, Connect/OAuth, Account Registration, EDI, Digital Certificate, Webhooks — backed by official SDKs in PHP, Java, Ruby, and .NET, plus WooCommerce, Magento / Adobe Commerce, and PrestaShop plugins and the PlugPag Android terminal SDK.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/pagseguro/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-pagseguro&utm_content=repo) · [Use as a Tool with Claude / Anthropic MCP](https://www.anthropic.com/news/model-context-protocol)

## Tags

- Payments, Checkout, Pix, Boleto, Cards, Subscriptions, Recurring, POS, Card Reader, Marketplace, Split, Payouts, Digital Bank, Brazil, Latin America, Fintech

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Environments

| Environment | Base URL | Notes |
|---|---|---|
| Production | `https://api.pagseguro.com` | Live merchants, real settlements |
| Sandbox | `https://sandbox.api.pagseguro.com` | Free for development, certification, and testing |

Authentication: Bearer access token issued via the developer portal or the Connect OAuth flow. HTTPS is required end to end. mTLS via the Digital Certificate API is available as a higher-trust option for Pix Bacen and payouts.

## APIs

### PagBank Orders API
Core REST surface for creating and managing orders and their associated charges across credit card, debit card with 3DS, boleto, and Pix. Covers capture, cancel, refund, fees retrieval, and stored-card validation.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [API Reference](https://developer.pagbank.com.br/reference/introducao)
- [OpenAPI](openapi/pagseguro-openapi.yml)

### PagBank Checkout & Payment Link API
Hosted checkout and shareable payment-link generation. Merchants create, activate, deactivate, and retrieve checkouts; PagBank renders the UI, handles payment-method selection and 3DS, and returns the buyer to the merchant on completion.

- [Documentation](https://developer.pagbank.com.br/docs/checkout)
- [OpenAPI](openapi/pagseguro-openapi.yml)

### PagBank Public Keys API
Issues the public keys used for client-side card encryption in PagBank's transparent checkout so raw PAN never reaches merchant servers.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [OpenAPI](openapi/pagseguro-openapi.yml)

### PagBank Recurring / Subscriptions API
Recurring-billing surface with plans, subscribers, subscriptions, invoices, coupons, refunds, and retry management. Supports activate, suspend, cancel, and per-subscriber payment-method updates.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [OpenAPI](openapi/pagseguro-openapi.yml)

### PagBank Pix API
Pix (Brazilian Central Bank instant-payment rail) charge creation and collection — QR-code generation, due-date Pix (Pix Cobrança), and payment status retrieval, integrated into the Orders flow.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)

### PagBank Boleto API
Boleto Bancário issuance and collection — generates a printable / scannable boleto tied to an Order, with status callbacks once the buyer pays at a bank, lottery house, or via internet banking.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)

### PagBank Marketplace / Split API
Payment-division (split) settlement for marketplaces and platforms — splits a single charge across multiple receivers (with optional custody / release control) so each seller is settled directly by PagBank.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)

### PagBank Connect / OAuth API
OAuth-style authorisation surface that lets a third-party application act on behalf of a PagBank account holder. SMS and challenge verification, access-token issuance, refresh, and revoke.

- [Documentation](https://developer.pagbank.com.br/docs/connect)
- [OpenAPI](openapi/pagseguro-openapi.yml)

### PagBank Account Registration API
Lets PagBank partners create and query merchant accounts on behalf of third parties — the on-ramp for platforms that want to onboard sub-merchants into the PagBank ecosystem.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [OpenAPI](openapi/pagseguro-openapi.yml)

### PagBank EDI API
Electronic Data Interchange surface for downloading transaction and settlement statements for reconciliation — a structured replacement for manual CSV/PDF statement processing.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)

### PagBank Digital Certificate (mTLS) API
Issues digital certificates for mTLS authentication, layered on top of bearer-token auth for higher-trust integrations and sensitive payouts / Pix Bacen flows.

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)

### PagBank Webhooks / Notifications
Event-driven notifications for order, charge, subscription, refund, and checkout state changes. Webhooks are signed so receivers can verify authenticity end to end.

- [Documentation](https://developer.pagbank.com.br/docs/webhooks)

## SDKs and Plugins

| Language / Platform | Repository |
|---|---|
| PHP | [pagseguro/pagseguro-sdk-php](https://github.com/pagseguro/pagseguro-sdk-php) |
| Java | [pagseguro/pagseguro-sdk-java](https://github.com/pagseguro/pagseguro-sdk-java) |
| Ruby | [pagseguro/pagseguro-sdk-ruby](https://github.com/pagseguro/pagseguro-sdk-ruby) |
| .NET / C# | [pagseguro/pagseguro-sdk-dotnet](https://github.com/pagseguro/pagseguro-sdk-dotnet) |
| Android — PlugPag (Bluetooth) | [pagseguro/plugpag](https://github.com/pagseguro/plugpag) |
| Android — PlugPagServiceWrapper (Moderninha / Minizinha) | [pagseguro/pagseguro-sdk-plugpagservicewrapper](https://github.com/pagseguro/pagseguro-sdk-plugpagservicewrapper) |
| WooCommerce | [pagseguro/pagbank-for-woocommerce](https://github.com/pagseguro/pagbank-for-woocommerce) |
| Magento / Adobe Commerce | [pagseguro/payment-magento](https://github.com/pagseguro/payment-magento) |
| PrestaShop | [pagseguro/pagseguro-modulo-prestashop](https://github.com/pagseguro/pagseguro-modulo-prestashop) |
| Postman Collection | [PagSeguro APIs (Postman)](https://documenter.getpostman.com/view/10863174/TVetc6HV) |

## Pricing

PagBank's cost surface is dominated by **per-transaction MDR** on cards, **per-transaction fees** on Pix and boleto, and **anticipation discounts** on card receivables — not per-API-call billing. API access itself is free in both sandbox and production. See the published merchant pricing at [pagbank.com.br/tarifas](https://pagbank.com.br/tarifas) for the live numbers.

Structured: [plans/pagseguro-plans-pricing.yml](plans/pagseguro-plans-pricing.yml) (API Commons Plans 0.1)

## Rate Limits

PagBank does not publish detailed per-tier QPS envelopes. Throttling is enforced per OAuth client / merchant account, with stricter envelopes on the regulated Pix Bacen and payouts rails. Scaffolded envelopes are captured in [rate-limits/pagseguro-rate-limits.yml](rate-limits/pagseguro-rate-limits.yml) (API Commons Rate Limits 0.1) for governance modelling — reconcile against your own production observations and the commercial agreement.

## FinOps

A FOCUS-shaped mapping for ingesting PagBank settlement statements (EDI API) into a FinOps data plane is available at [finops/pagseguro-finops.yml](finops/pagseguro-finops.yml). Cost domains: Card Processing, Pix Processing, Boleto Processing, Credit Anticipation, and API Consumption.

## Common Links

- [PagBank — Consumer](https://pagbank.com.br/)
- [PagSeguro — Brand](https://pagseguro.uol.com.br/)
- [Developer Portal](https://developer.pagbank.com.br/)
- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [API Reference](https://developer.pagbank.com.br/reference/introducao)
- [Getting Started (Primeiros Passos)](https://developer.pagbank.com.br/docs/primeiros-passos-pagbank)
- [Authentication](https://developer.pagbank.com.br/v1/docs/dev-autenticacao)
- [Available Environments](https://developer.pagbank.com.br/docs/ambientes-disponiveis)
- [Webhooks](https://developer.pagbank.com.br/docs/webhooks)
- [Changelog](https://developer.pagbank.com.br/changelog)
- [GitHub Organization](https://github.com/pagseguro)
- [PagSeguro Investor Relations (NYSE: PAGS)](https://investors.pagseguro.com/)
- [Postman Collection](https://documenter.getpostman.com/view/10863174/TVetc6HV)

## Artifacts

- [apis.yml](apis.yml) — APIs.json catalog entry
- [openapi/pagseguro-openapi.yml](openapi/pagseguro-openapi.yml) — OpenAPI 3.1 specification
- [plans/pagseguro-plans-pricing.yml](plans/pagseguro-plans-pricing.yml) — API Commons Plans 0.1
- [rate-limits/pagseguro-rate-limits.yml](rate-limits/pagseguro-rate-limits.yml) — API Commons Rate Limits 0.1
- [finops/pagseguro-finops.yml](finops/pagseguro-finops.yml) — FOCUS-aligned FinOps profile
- [review.yml](review.yml) — apis.yml validation summary

---

*Maintained by [API Evangelist](https://apievangelist.com). Designed for use with [Naftiko governed AI capabilities](https://github.com/naftiko/fleet) and with [Anthropic's Model Context Protocol](https://www.anthropic.com/news/model-context-protocol) so Claude and other agents can invoke PagBank APIs as governed tools.*
