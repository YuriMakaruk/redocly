# User Registration & Onboarding Guide

This guide walks new customers through the full onboarding process in Chaching - from email verification to Stripe migration and subscription selection.

# Prerequisites

Before onboarding into Chaching, the user must complete the following:

**Required Accounts**

| Prerequisite | Description |
| --- | --- |
| **Amazon Web Services account** | Required to verify sender email and receive the verification link used in the first step. For details, refer to Step 1. |
| **Stripe account** | Required if the user is migrating existing subscriptions from Stripe. |

# **Account Creation**

### **Step 1 — Verify Email (AWS SES)**

1. Open the verification email from **Amazon Web Services**.
2. Click **Verify Email Address**.
3. You will receive confirmation:
    
    *“You have successfully verified an email address. You can now start sending email from this address.”*
    

# **Starting the Chaching Sign-Up Flow**

### **Step 2 — Open Chaching Sign-Up**

1. Navigate to:

[**https://test.chaching.io/sign-up**](https://test.chaching.io/sign-up)

1. Enter the email address you previously verified and click **Continue**.

Alternatively, from the sign-in page click **Get Started**.

### **Step 3 — Verify Email for Chaching**

A screen will prompt you to confirm your email.

{% img src="./images/confirm.png" alt="confirm.png" withLightbox=true width="" height="" /%}

Open the email from Chaching and click **Verify Email**.

You will then be redirected to:

[**https://test.chaching.io/onboarding/personal-info**](https://test.chaching.io/onboarding/personal-info)

# **Onboarding Flow Overview**

The complete onboarding flow consists of:

1. **Personal info**
2. **Add branding**
3. **Replace current solution**
4. **Stripe migration**
5. **Subscription selection**
6. **Review**
7. **Pricing**

# **Step 1: Personal Info**

### 

| Section | Fields / Description | Required |
| --- | --- | --- |
| **Email verification** | Confirms that the user email is verified. | yes |
| **Your full name** | Text input. | yes |
| Phone |  | yes |
| **Company name** | Text input. | yes |
| **Business address** | Text input. | yes |
| **Set password** | Enter password + repeat password fields. | yes |
| Password requirements | - 8 characters long - 1 uppercase letter - 1 number - 1 special character | yes |

# **Step 2: Add Branding**

| Section | Fields / Description | Required |
| --- | --- | --- |
| **Logo upload** | Drag & drop or file picker. 
Supported: PNG/JPEG, up to 2 MB. | yes |
| **Brand color** | Primary brand color picker. | yes |
| **Accent color** | Accent color picker. | yes |
| **Preview** | Shows branding applied to sample subscription card (e.g., “CC $200/month”). |  |
| **Payment form** | Cardholder name, card number, expiry, CVC, ZIP, country. |  |
| **Save changes** | Saves branding info. |  |

## 

# **Step 3: Replace Current Solution**

Users must choose how they were previously using Stripe:

### **Integration Type Options**

1. **Hosted page** (Stripe Checkout or similar)
2. **API solution** (custom Stripe API integration)
3. **Both**

The selected option determines the next steps.

## **Option 1: Replace Hosted Page**

The page displays:

| Item | Description |
| --- | --- |
| **Hosted page** | Preview your current Stripe-hosted payment link. |
| **Embedded solution** | Provides the Chaching embedded payment link. |
| **Copy link** | Copy the link:
[https://test.chaching.io/process-payment/{token}](https://test.chaching.io/process-payment/%7Btoken%7D)
Note: {token} should be replaced with the actual payment token. |
| **External page** | Provides the link for external page usage. |
| **I replaced the link**  | Confirmation to move to the next step. |

## **Option 2: Replace API Endpoints**

The user is instructed to:

1. Go to **Chaching documentation**.
2. Replace all Stripe billing and invoicing endpoints with Chaching’s equivalents.
    
    (Chaching mimics Stripe’s API structure.)
    
3. Return to onboarding once complete.

The button **Continue** moves to migration step.

# **Step 4: Stripe Migration**

### **Migration Options**

1. Users choose one of the options and clicks **Continue**:
- **Migrate from Stripe**
- **I do not have existing subscriptions**
1. Learn how the import works and then click **I understand**

## **Import existing data from Stripe**

Chaching import flow:

1. Provide Stripe public and secret keys and click **Continue**.
2. Chaching imports subscription data (customers, products, taxes).
3. The user selects which subscriptions to migrate.
4. Selected subscriptions are deleted from Stripe.
5. New billing becomes active from the next billing cycle.

User must click **I understand** to proceed.

## **Import Existing Data**

Steps shown:

1. Navigate to Stripe Dashboard.
2. Reveal and copy the public + secret keys.
3. Paste them into the Chaching form.

**Note:**

Stripe keys are used **only for one-time import** and never stored.

After this step, the developer mentioned the process will contain:

- **Customer synchronization**
- **Subscription selection**
- **Subscription synchronization**

This section will also feature a **progress bar**.

# **Step 5: Subscription Selection**

*(Available once developer completes the workflow)*

The user will:

- See imported subscriptions
- Select which subscriptions to enable
- Assign plans or products if required
- Confirm mappings before migration

A progress indicator will show import status.

# **Step 6: Review**

*(You have not reached this step yet — placeholder)*

The Review page will include:

- Personal info summary
- Branding summary
- Integration selection
- Stripe migration summary
- Subscription choices

The user will confirm all details before continuing to Pricing.

# **Step 7: Pricing**

*(Placeholder — not reached)*

This page will likely include:

- Selected plan
- Cost breakdown
- Billing interval
- Payment method
- Final confirmation

# **Completion**

After submitting the Pricing page, the account is fully onboarded and can begin using:

- Chaching Payment Links
- Subscriptions
- API endpoints
- Branding configuration
- Dashboard tools
