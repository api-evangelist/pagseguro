# PagSeguro / PagBank (pagseguro)

PagSeguro (operating consumer-facing under the PagBank brand) is one of Brazil's largest payment processors and digital-banking platforms. Originally spun out of UOL (Universo Online) and listed on the NYSE under PAGS, the company offers an end-to-end financial stack covering online payments, in-person card acceptance via the Moderninha and Minizinha terminal families, Pix instant payments, boleto, credit and debit cards, recurring subscriptions, marketplace split, payouts, account-as-a-service, and a digital bank with cards, credit, and investments. Its developer portal at developer.pagbank.com.br exposes a REST API surface (Orders, Charges, Public Keys, Checkout, Recurring, Connect/OAuth, Account Registration, EDI, Webhooks) backed by official SDKs in PHP, Java, Ruby, and .NET, plus WooCommerce, Magento/Adobe Commerce, and PrestaShop plugins.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/pagseguro/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/pagseguro/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Producer
- **Access:** 3rd-Party

## Tags

- Payments
- Checkout
- Pix
- Boleto
- Cards
- Subscriptions
- Recurring
- POS
- Card Reader
- Marketplace
- Split
- Payouts
- Digital Bank
- Brazil
- Latin America
- Fintech

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### PagBank Orders API

Core REST surface for creating and managing orders and their associated charges across credit card, debit card with 3DS, boleto, and Pix. Covers capture, cancel, refund, fees retrieval, and stored-card validation.

- **Human URL:** [https://developer.pagbank.com.br/reference/criar-pedido](https://developer.pagbank.com.br/reference/criar-pedido)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Orders
- Payments
- Refunds
- 3DS

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [API Reference](https://developer.pagbank.com.br/reference/introducao)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Checkout & Payment Link API

Hosted checkout and shareable payment-link generation. Merchants create, activate, deactivate, and retrieve checkouts; PagBank renders the UI, handles payment-method selection and 3DS, and returns the buyer to the merchant on completion.

- **Human URL:** [https://developer.pagbank.com.br/docs/checkout](https://developer.pagbank.com.br/docs/checkout)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Checkout
- Hosted
- Payment Links

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/checkout)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Public Keys API

Issues the public keys used for client-side card encryption in PagBank's transparent checkout. Lets merchants tokenise card data in the browser so raw PAN never reaches their servers.

- **Human URL:** [https://developer.pagbank.com.br/reference/criar-uma-chave-publica](https://developer.pagbank.com.br/reference/criar-uma-chave-publica)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Tokenization
- Encryption
- PCI

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Recurring / Subscriptions API

Recurring-billing surface with plans, subscribers, subscriptions, invoices, coupons, refunds, and retry management. Supports activate, suspend, cancel, and per-subscriber payment-method updates.

- **Human URL:** [https://developer.pagbank.com.br/reference/criar-plano-recorrente](https://developer.pagbank.com.br/reference/criar-plano-recorrente)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Subscriptions
- Recurring
- Plans
- Invoices

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Pix API

Pix (Brazilian Central Bank instant-payment rail) charge creation and collection. Supports QR-code generation, due-date Pix (Pix Cobrança), and payment status retrieval, integrated into the Orders flow.

- **Human URL:** [https://developer.pagbank.com.br/reference/criar-um-pedido-pix](https://developer.pagbank.com.br/reference/criar-um-pedido-pix)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Pix
- Instant Payments
- QR
- Brazil

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Boleto API

Boleto Bancário issuance and collection. Generates a printable / scannable boleto tied to an Order, with status callbacks once the buyer pays at a bank, lottery house, or via internet banking.

- **Human URL:** [https://developer.pagbank.com.br/reference/criar-pedido-com-boleto](https://developer.pagbank.com.br/reference/criar-pedido-com-boleto)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Boleto
- Brazil
- Collections

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Marketplace / Split API

Payment-division (split) settlement for marketplaces and platforms. Splits a single charge across multiple receivers (with optional custody / release control) so each seller is settled directly by PagBank.

- **Human URL:** [https://developer.pagbank.com.br/reference/criar-pedido-com-split](https://developer.pagbank.com.br/reference/criar-pedido-com-split)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Marketplace
- Split
- Settlement

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Connect / OAuth API

OAuth-style authorisation surface that lets a third-party application act on behalf of a PagBank account holder. Includes SMS and challenge verification, access-token issuance, refresh, and revoke.

- **Human URL:** [https://developer.pagbank.com.br/docs/connect](https://developer.pagbank.com.br/docs/connect)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- OAuth
- Authorization
- Connect

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/connect)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Account Registration API

Lets PagBank partners create and query merchant accounts on behalf of third parties — the on-ramp for platforms that want to onboard sub-merchants into the PagBank ecosystem.

- **Human URL:** [https://developer.pagbank.com.br/docs/cadastro-de-clientes](https://developer.pagbank.com.br/docs/cadastro-de-clientes)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- Onboarding
- Sub Merchants
- KYC

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank EDI API

Electronic Data Interchange surface for downloading transaction and settlement statements for reconciliation — a structured replacement for manual CSV/PDF statement processing.

- **Human URL:** [https://developer.pagbank.com.br/docs/edi](https://developer.pagbank.com.br/docs/edi)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- EDI
- Reconciliation
- Statements

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Digital Certificate (mTLS) API

Issues digital certificates for mTLS authentication, layered on top of bearer-token auth for higher-trust integrations and sensitive payouts / Pix Bacen flows.

- **Human URL:** [https://developer.pagbank.com.br/docs/certificado-digital](https://developer.pagbank.com.br/docs/certificado-digital)
- **Base URL:** `https://api.pagseguro.com`

#### Tags

- mTLS
- Security
- Certificates

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Webhooks / Notifications

Event-driven notifications for order, charge, subscription, refund, and checkout state changes. Webhooks are signed so receivers can verify authenticity end-to-end.

- **Human URL:** [https://developer.pagbank.com.br/docs/webhooks](https://developer.pagbank.com.br/docs/webhooks)
- **Base URL:** `customer-configured`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://developer.pagbank.com.br/docs/webhooks)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagSeguro PHP SDK

Official PHP integration library for PagSeguro / PagBank.

- **Human URL:** [https://github.com/pagseguro/pagseguro-sdk-php](https://github.com/pagseguro/pagseguro-sdk-php)
- **Base URL:** `https://github.com/pagseguro/pagseguro-sdk-php`

#### Tags

- SDK
- PHP

#### Properties

- [Repository](https://github.com/pagseguro/pagseguro-sdk-php)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagSeguro Java SDK

Official Java integration library for PagSeguro / PagBank.

- **Human URL:** [https://github.com/pagseguro/pagseguro-sdk-java](https://github.com/pagseguro/pagseguro-sdk-java)
- **Base URL:** `https://github.com/pagseguro/pagseguro-sdk-java`

#### Tags

- SDK
- Java

#### Properties

- [Repository](https://github.com/pagseguro/pagseguro-sdk-java)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagSeguro Ruby SDK

Official Ruby integration library for PagSeguro / PagBank.

- **Human URL:** [https://github.com/pagseguro/pagseguro-sdk-ruby](https://github.com/pagseguro/pagseguro-sdk-ruby)
- **Base URL:** `https://github.com/pagseguro/pagseguro-sdk-ruby`

#### Tags

- SDK
- Ruby

#### Properties

- [Repository](https://github.com/pagseguro/pagseguro-sdk-ruby)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagSeguro .NET SDK

Official .NET / C# integration library for PagSeguro / PagBank.

- **Human URL:** [https://github.com/pagseguro/pagseguro-sdk-dotnet](https://github.com/pagseguro/pagseguro-sdk-dotnet)
- **Base URL:** `https://github.com/pagseguro/pagseguro-sdk-dotnet`

#### Tags

- SDK
- .NET
- C#

#### Properties

- [Repository](https://github.com/pagseguro/pagseguro-sdk-dotnet)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank PlugPag (Terminal Integration)

Bluetooth / Android terminal integration for PagBank's Moderninha and Minizinha card readers, enabling third-party apps to drive in-person card and Pix payments on PagBank hardware.

- **Human URL:** [https://github.com/pagseguro/plugpag](https://github.com/pagseguro/plugpag)
- **Base URL:** `https://github.com/pagseguro/plugpag`

#### Tags

- POS
- Card Reader
- Android
- Bluetooth

#### Properties

- [Repository](https://github.com/pagseguro/plugpag)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank PlugPagServiceWrapper

Android service wrapper for integrating with the Moderninha / Minizinha terminal family — the official higher-level SDK on top of PlugPag.

- **Human URL:** [https://github.com/pagseguro/pagseguro-sdk-plugpagservicewrapper](https://github.com/pagseguro/pagseguro-sdk-plugpagservicewrapper)
- **Base URL:** `https://github.com/pagseguro/pagseguro-sdk-plugpagservicewrapper`

#### Tags

- POS
- Card Reader
- Android
- Kotlin

#### Properties

- [Repository](https://github.com/pagseguro/pagseguro-sdk-plugpagservicewrapper)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank for WooCommerce

Official WooCommerce plugin embedding PagBank checkout, Pix, boleto, and card payments in WordPress storefronts.

- **Human URL:** [https://github.com/pagseguro/pagbank-for-woocommerce](https://github.com/pagseguro/pagbank-for-woocommerce)
- **Base URL:** `https://github.com/pagseguro/pagbank-for-woocommerce`

#### Tags

- Plugin
- WooCommerce
- WordPress

#### Properties

- [Repository](https://github.com/pagseguro/pagbank-for-woocommerce)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagBank Payment for Magento / Adobe Commerce

Official Magento 2 / Adobe Commerce payment module for PagBank.

- **Human URL:** [https://github.com/pagseguro/payment-magento](https://github.com/pagseguro/payment-magento)
- **Base URL:** `https://github.com/pagseguro/payment-magento`

#### Tags

- Plugin
- Magento
- Adobe Commerce

#### Properties

- [Repository](https://github.com/pagseguro/payment-magento)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PagSeguro PrestaShop Module

Official PrestaShop transparent-checkout integration module for PagSeguro / PagBank.

- **Human URL:** [https://github.com/pagseguro/pagseguro-modulo-prestashop](https://github.com/pagseguro/pagseguro-modulo-prestashop)
- **Base URL:** `https://github.com/pagseguro/pagseguro-modulo-prestashop`

#### Tags

- Plugin
- PrestaShop

#### Properties

- [Repository](https://github.com/pagseguro/pagseguro-modulo-prestashop)
- [Postman Collection](collections/pagseguro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pagseguro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://pagbank.com.br/)
- [Consumer Website](https://pagseguro.uol.com.br/)
- [Developers](https://developer.pagbank.com.br/)
- [Documentation](https://developer.pagbank.com.br/docs/apis-pagbank)
- [API Reference](https://developer.pagbank.com.br/reference/introducao)
- [Getting Started](https://developer.pagbank.com.br/docs/primeiros-passos-pagbank)
- [Authentication](https://developer.pagbank.com.br/v1/docs/dev-autenticacao)
- [Environments](https://developer.pagbank.com.br/docs/ambientes-disponiveis)
- [Webhooks](https://developer.pagbank.com.br/docs/webhooks)
- [Changelog](https://developer.pagbank.com.br/changelog)
- [Git Hub](https://github.com/pagseguro)
- [Postman](https://documenter.getpostman.com/view/10863174/TVetc6HV) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Investor Relations](https://investors.pagseguro.com/)

## Maintainers

**FN:** API Evangelist
**URL:** https://apievangelist.com
