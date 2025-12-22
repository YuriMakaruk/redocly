# Introduction

Chaching is a modern subscription-billing platform designed to simplify product management, customer lifecycle workflows, and recurring payments.
It combines a clean dashboard for business users with a powerful API built for developers who need full automation and control.

Chaching is particularly useful for companies migrating away from Stripe’s subscription system, offering tools to import subscriptions and continue charging customers without disrupting existing billing cycles.

Chaching is built for users who:

* **Use the dashboard** to create products, manage customers, and monitor payment activity.
* **Integrate through the API** to automate subscription creation, billing, and customer lifecycle workflows.
* **Migrate existing Stripe subscriptions**, ensuring a smooth transition to Chaching as the new billing engine.

Chaching serves two main user groups:

* **Business / Admin Users** – manage products, pricing, subscriptions, customers, and see payment activity.
* **Developers** – integrate backend systems with Chaching through REST APIs to automate billing workflows.

## System Overview

Chaching includes two primary components:

**Dashboard**

A user interface where businesses can:

* Create products and prices
* Manage customer profiles
* View subscriptions and payment history
* Trigger or monitor migrations from Stripe

**REST API**

A programmable interface allowing developers to:

* Create and manage customers
* Automate subscription creation
* Generate invoices
* Process payments and renewals

The dashboard and API are fully connected — changes made in one are instantly reflected in the other.

<!--
## Entities

{% partial file="/_partials/entities.md" /%}
-->

## Release Notes

<aside>
💡 MVP version. Core subscription, product, and customer management are live. Payments integration in progress.

</aside>

<aside>
💡 Current Limitation:
Only flat-rate pricing is supported. Tiered, package, and usage-based models will be added in future releases.

</aside>
<br>

**Supported Pricing Models (MVP)**

- **Flat rate — Supported**
- **Tiered — Not supported (coming soon)**
- **Package/bulk — Not supported (coming soon)**
- **Usage-based/metred — Not supported (coming soon)**

## Need Help?
Refer to:
- [Documentation](./index.md)
- [Contact Support](./Support&Communication.md)
- [FAQ](./Support&Communication.md)

<!--
## Tiered Pricing 

Chaching will support multiple tiers, per-unit pricing, and volume discounts.

Expected release: Q1 2026
-->
