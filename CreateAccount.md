# Adding Account

## Overview

Chaching supports **multiple accounts per user**. Each account is fully isolated and has its own Stripe integration, customers, subscriptions, products, invoices, and billing data.

There is **no limit** to the number of accounts you can create.

## When to Add a New Account

You should create a new account if you need to:

* Manage a **separate Stripe account**
* Keep **test and production data isolated**
* Operate **multiple brands or business units**
* Manage **client accounts** (agency or reseller model)


## How to Add a New Account

1. Go to **Your Account**
2. Click **Add an Account**
   {% img src="./images/AddNewAccount.png" alt="AddNewAccount.png" withLightbox=true width="" height="" /%}
3. You are redirected to the onboarding flow

The full step-by-step onboarding process (account details, Stripe connection, migration, bank setup) is described in [User Registration & Onboarding Guide](./onboarding.md).


## Sandbox vs Live Accounts

During account creation, you can mark the account as **Sandbox**.

* Sandbox accounts follow the same onboarding steps
* Once completed, the Dashboard clearly shows **Test Mode**
* Sandbox and live accounts are fully isolated

## Important MVP Limitations

⚠️ **Incomplete setup deletes the account**

* If you exit onboarding after creating an account but before completion, the account is **automatically deleted**
* Deleted accounts **cannot be recovered**
* You must restart the account creation process

⚠️ **No account limit**

* You can create **unlimited accounts**
* Each account requires its own valid Stripe credentials

## Switching Between Accounts

Use the **Account Selector** to switch accounts.

When switching accounts:

* Customers, subscriptions, invoices, and metrics change
* Active Stripe connection changes

What stays the same:

* Your user profile
* Login credentials
* Personal settings

## Data Isolation

Each account is completely isolated:

* Data from one account is never visible in another
* Stripe operations affect only the active account
* Reports and analytics are account-specific





