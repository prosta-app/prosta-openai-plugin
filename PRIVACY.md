# Privacy for the Prosta connector

This notice explains the Prosta connector's data flow alongside the
[Prosta privacy policy](https://www.prosta.app/privacy) and
[terms](https://www.prosta.app/terms). It applies to the read-only Prosta
integration you choose to connect in ChatGPT, Codex, or Claude.
This supplement governs the connector-specific sharing and additional AI-host
recipients described here; the base policy covers general Prosta use. General
recipient descriptions in the base policy do not exclude the AI host you
choose for this integration.

## What is shared and why

Public discovery sends the task's search terms and selected public business,
service, and professional identifiers, plus requested availability dates, to Prosta.
Results contain the public
business profile, published catalog information, professionals, and available
times needed to answer the request. A host may provide a coarse city hint
through its controlled metadata for a requested nearby search. The hint is
optional; the connector does not request GPS coordinates or personal addresses.

With your explicit Prosta consent for `appointments:read`, the connector also
returns your own appointment information: booking identifiers and status,
business and professional details, dates and times, services, duration, and
prices. It uses your account identity internally to check access. Consent does
not permit another customer's records, a business administration role, or
booking changes. Public discovery does not require appointment access.

Your chosen AI host—OpenAI for ChatGPT or Codex, or Anthropic for Claude—receives
the tool results to answer your request. This transfer is part of using the
integration. The host processes your conversation and returned data under its
own account settings and privacy policy:
[OpenAI Privacy Policy](https://openai.com/policies/privacy-policy/) or
[Anthropic Privacy Policy](https://www.anthropic.com/legal/privacy).
Your host may retain chat history
separately from Prosta. Avoid unnecessary private information in searches or
conversations; never provide passwords, OTPs, or access tokens in chat.

## Access, expiry, and stored records

You review the account, integration, and permission in Prosta before approving.
The current connector configuration expires access tokens after five minutes,
authorization codes after one minute, and unfinished consent interactions after
ten minutes. Refresh credentials and connection sessions have a one-day
provider lifetime. A recorded consent is valid for at most 30 days and may end
sooner when revoked or when the associated session expires.

Expiry prevents use of the expired credential; it is not a promise that the
stored record is physically deleted at that moment. Expired provider records
are cleaned up in bounded batches during subsequent provider writes. Consent
history remains until account deletion. This notice does not assert a separate
logging retention duration or an immediate physical cleanup deadline.

MCP responses use `Cache-Control: private, no-store`. This HTTP instruction does
not delete host conversations or override the host's retention controls.
Ordinary Prosta booking records remain part of your Prosta account; connecting
or disconnecting the integration does not delete your appointments.

## Your controls

Remove access through Prosta Profile → Connected apps, then disconnect the
integration in your AI host. Revocation blocks future private reads and removes
the associated token family. It cannot erase records already returned to the
host. Use that host's account and conversation controls for its retained data.
To switch Prosta accounts, revoke the previous connection and sign in with the
intended account before granting consent again.

Prosta's account-deletion workflow removes the account's connector provider
state and consent history. For access, deletion, or privacy questions, contact
[Prosta Support](https://www.prosta.app/support). Do not include credentials or
customer records in a public repository issue. See [Security](./SECURITY.md)
for private reporting guidance.
