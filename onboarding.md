# User Registration & Onboarding Guide

The ChaChing onboarding process guides you through setting up your account, configuring your branding, selecting your integration type, importing data from Stripe, and reviewing all changes before completing your migration. Before you begin, it’s helpful to understand what happens once the migration is confirmed, as this ensures a smooth transition and clear expectations.

**What Happens After You Confirm the Migration**

When you complete the onboarding flow and approve the migration, ChaChing automatically handles all required steps behind the scenes:

1. **Your imported Stripe subscriptions will be cancelled in Stripe.**
    
    ChaChing takes over billing responsibility while preserving your historical records.
    
2. **Subscriptions will be billed on their normal renewal dates.**
    
    Any past-due subscriptions will be retried automatically after migration.
    
3. **ChaChing will sync all necessary dependencies**, including:
    - Customers
    - Tax rates
    - Product lists
    - Related metadata
4. **The sync process may take some time.**
    
    During this period, customers can continue creating new subscriptions. ChaChing will monitor your Stripe account and import these automatically. You will receive a notification once the full import and synchronization are complete.
    
5. **Your historical Stripe data remains intact.**
    
    Nothing is deleted from your Stripe dashboard—your past information stays available for safe keeping and audit purposes.

# Prerequisites
Before onboarding into Chaching, the user must create the following:

| Prerequisite | Description |
| --- | --- |
| **Email account** | Required to verify your email and receive the verification link for Step 1. |
| **Stripe account** | Required if you plan to migrate existing subscriptions from Stripe. |

# Account Creation

## The Sign-Up Flow

1. Navigate to:
    
    [**https://test.chaching.io/sign-up**](https://test.chaching.io/sign-up)
    
2. Enter the email address and click **Continue with email**.

{% img src="./images/Sign-Up.png" alt="Sign-Up.png" withLightbox=true width="" height="" /%}

Alternatively, from the sign-in page click **Get Started**.

{% img src="./images/GetStarted.png" alt="GetStarted.png" withLightbox=true width="" height="" /%}

You will be prompted to verify your email.

{% img src="./images/prompt.png" alt="prompt.png" withLightbox=true width="" height="" /%}

Open the email from Chaching and click Verify Email.

{% img src="./images/email.png" alt="email.png" withLightbox=true width="" height="" /%}

Once you click the link, you’ll be securely redirected back to ChaChing Onboarding screen.

{% img src="./images/onboard.png" alt="onboard.png" withLightbox=true width="" height="" /%}

# Onboarding Flow

The complete onboarding flow consists of:

1. **Personal info**
2. **Branding**
3. **Integration Type**
4. **Stripe Migration**
5. **Subscription Selection**
6. **Review**
7. **Pricing**

## Step 1: Personal Info

After verifying your email, you’ll be asked to provide:

- Personal details
- Business address
- Password

Fill in all required fields and click **Continue**.

**Personal Information — Field Reference**

| **Name** | **Description** | **Required / Optional** |
| --- | --- | --- |
| **Full Name** | Your first and last name used for account identification. | **Required** |
| **Phone** | Contact phone number. Must be a valid phone format. | **Required** |
| **Company Name** | The legal or business name of your company. | **Required** |
| **Country** | Select your country of operation from the dropdown list. | **Required** |
| **Address Line 1** | Primary business address. Must contain at least 2 characters. | **Required** |
| **Address Line 2** | Secondary address information, such as suite or unit number. | Optional |
| **City** | City where your business operates. Must contain at least 2 characters. | **Required** |
| **State / Region** | State, province, or region. Must contain at least 2 characters. | **Required** |
| **Zip / Postal Code** | Postal code for your business address. Must be valid for the selected country. | **Required** |
| **Password** | Must meet all requirements: 8 characters, 1 uppercase, 1 number, 1 special character. | **Required** |
| **Password Confirmation** | Enter the same password again to confirm. Must match the password. | **Required** |

## Step 2: Branding

In this step, you can personalize the look and feel of your tenant.

**You can:**

- Upload your company logo
- Choose your primary and accent colors
- Preview how your branding will look in ChaChing

Click **Continue** once you’re satisfied with the preview.

**Branding – Field Reference**

| **Name** | **Description** | **Required / Optional** |
| --- | --- | --- |
| **Logo** | Upload your company logo. Supports PNG and JPEG formats up to 2 MB. | **Required**  |
| **Set Default Logo** | Use ChaChing’s default logo if no custom logo is uploaded. | Optional |
| **Primary Brand Color** | Main color used across your customer-facing pages. Select from color picker. | **Required** |
| **Accent Color** | Secondary color used for highlights and UI accents. Select from color picker. | **Required** |
| **Save Changes** | Saves all branding updates and applies them to your tenant preview. | — |

Note: the branding can be personalized in the tenant profile settings. For details, refer to 

## Step 3. Integration Type

In this step, you select how your platform currently processes payments. ChaChing supports multiple integration models, so choosing the correct one ensures you receive the correct setup instructions in the next steps.

You will see three options:

- **Hosted Page** – if you use Stripe Checkout or similar hosted payment pages.
- **API Solution** – if your system directly integrates with Stripe’s Billing APIs.
- **Both** – if you use both hosted checkout and direct API calls.

After selecting an option, click **Continue** to proceed.

### Option 1: Replace Hosted Page

If you selected **Hosted Page** or **Both**, you will receive instructions to replace your existing Stripe Checkout link.

You can:

- Copy your new ChaChing Checkout link
- Use the embedded version or the external hosted page
- Confirm all previous Stripe URLs have been replaced

Click **I replaced the link** when complete.

### Option 2: Replace API Endpoints

If you selected **API Integration**, ChaChing will explain how to replace your Stripe API calls with ChaChing API calls.

You’ll find:

- A link to the API documentation
- A mapping overview showing that ChaChing uses a Stripe-compatible format
- A confirmation step to proceed once you’ve updated your integration

Click **Continue** to proceed.

## Step 4: Stripe Migration

If you already have active Stripe customers, ChaChing can import them for you.

Сhoose between:

- **Migrate from Stripe**
- **I don’t have existing subscriptions**

If you don't have existing subscriptions, this part of onboarding will be skipped.

### 4.1 Connect Your Stripe Account

To import subscriptions, provide your Stripe keys:

- Stripe Secret Key
- Stripe Public Key

Once validated, ChaChing will fetch your subscriptions so you can decide which ones to migrate.

Click **Continue**.

## Step 5: Subscription Selection

You will see a table of all subscriptions retrieved from Stripe.
{% img src="./images/2025-12-09_14-49-59.png" alt="2025-12-09_14-49-59.png" withLightbox=true width="" height="" /%}

Here you can:

- Select all subscriptions
- Select only active subscriptions
- Select first 100
- Select individually
- Review amounts, dates, customer names, emails, and billing cycles

A summary panel shows how many subscriptions you’ve selected and their total monthly value.

Click **Continue** when ready.

**Select Subscriptions – Field Reference**

| **Name** | **Description** |
| --- | --- |
| **Subscription ID** | Unique identifier of the subscription imported from Stripe. Used to map and migrate subscription records into ChaChing. |
| **Status** | Current subscription state (e.g., active, trialing, past_due). Helps determine which subscriptions are eligible for migration. |
| **Customer Name** | Full name of the customer associated with the subscription. |
| **Customer Email** | Email address of the customer. Used for billing communication and subscription mapping. |
| **Start Date** | The date when the subscription originally started in Stripe. |
| **Frequency** | Billing frequency (e.g., monthly, yearly). |
| **Renewal Date** | The next billing date when the subscription will renew after migration. |
| **Amount** | Price the customer is currently paying for the subscription. |

## Step 6: Review Migration Summary

In this step, ChaChing calculates your expected monthly savings compared to Stripe.

{% img src="./images/2025-12-09_14-53-34.png" alt="2025-12-09_14-53-34.png" withLightbox=true width="" height="" /%}
You’ll see:

- A comparison of Stripe’s 0.7% fee vs ChaChing’s 0.35% fee
- An estimated monthly savings amount based on the subscriptions you imported

Below the savings section, you’ll be asked to connect your bank account.

### 6.1 Connect Your Bank

To receive payouts, connect your bank account via Plaid.

When completed successfully, the screen will display:

- Bank name
- Masked account number
- A confirmation badge

Сlick **Continue**.

## 7. Review All Changes

In the final step, you will see a full summary of everything that will be migrated:

- Number of subscriptions
- Number of customers
- Number of products
- Sales tax details
- Total subscription value
- Amount saved per month after moving from Stripe to ChaChing based on current subscription fees.

Review all information carefully.

Once you a**ccept and continue**, your tenant will be activated and you will be redirected to your ChaChing dashboard.