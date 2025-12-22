# Developer Settings

The **Developer Settings** page allows developers to manage API access credentials and configure event-driven integrations.

## API Keys

This section provides access to standard API keys used to authenticate requests to the ChaChing API.

### Keys

| **Field** | **Description** |
| --- | --- |
| **Published key** | Public API key used in client-side integrations (e.g., `pk_3NKx7UOLI3MKgGwLqAJmKYDMSyXaKel5Kjb0Y6gDSfz7jBrB-XAW0B0OYkiG1trRmzpCAhYqKXJSTCOeVU9S4A`). |
| **Secret key** | Private API key used for server-side requests. Displayed in a masked format (e.g., `sk_Ew2Ww****C9JwORcw...`). |

### Actions

| **Action** | **Description** |
| --- | --- |
| **Copy to clipboard** | Copies the selected API key (published or secret) to the clipboard. |

### Security Notes

- The **Secret key** must never be exposed in client-side code.
- If a secret key is compromised, it should be rotated immediately.
- Access to API keys should be restricted to authorized users only.

## Webhooks

### Notes

- Webhooks are not yet available for configuration.
- Once enabled, webhooks will allow real-time notifications for events such as payments, invoices, and subscription updates.
- Future releases are expected to include webhook endpoint configuration, event selection, and delivery logs.