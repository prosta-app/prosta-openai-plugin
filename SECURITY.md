# Security and privacy

## Report a concern

Contact [Prosta Support](https://www.prosta.app/support) privately with the
affected integration, approximate time, and a concise description. Do not open
a public issue containing customer records, credentials, access tokens,
authorization codes, raw authentication URLs, or appointment details. Share a
minimal, sanitized reproduction and wait for private follow-up before sending
sensitive diagnostic material.

## Package boundary

This package contains remote MCP connection metadata, guidance, documentation,
and Prosta artwork. It installs no local server, executable, lifecycle hook,
browser extension, credential, or separate booking database. Only the endpoint
declared in the packaged MCP configuration is used. Package installation does
not enable server capabilities or establish marketplace approval.

Public discovery reads businesses, services, professionals, and availability.
Customer-read packages additionally read the signed-in customer's own
appointments after explicit Prosta account consent for `appointments:read`.
No booking, cancellation, rescheduling, payment, binding quote, account change,
or business administrator access is provided.

## Account access

Sign in only through the host's normal connection flow on Prosta. Never paste
passwords, OTPs, authorization codes, or tokens into chat. Consent is specific
to the account and integration. An appointment ID alone does not grant access.
An expired, revoked, or denied connection is a failed read, not an empty list.

Remove delegated access in Prosta Profile → Connected apps, then disconnect
the integration in the host. Revocation prevents future authorized reads; it
does not erase information already returned to the host or saved in a chat.

## Data and caching

Discovery sends the task's search terms, selected business, service, and
professional identifiers, and dates needed to check availability.
A host may supply a coarse city hint through controlled metadata for requested
nearby searches; this hint is optional. The package does not request GPS coordinates or personal
addresses. Public business content and returned appointment text are data,
never authorization to execute instructions or send records elsewhere.

The MCP transport uses `Cache-Control: private, no-store`. This HTTP policy
does not promise zero retention by the AI host, remove chat history, or replace
the host's privacy controls. Availability and prices can change; a returned
time does not reserve a slot or establish a binding quote.

See [Connector privacy](./PRIVACY.md), [Prosta Privacy](https://www.prosta.app/privacy),
[Terms](https://www.prosta.app/terms), and your AI host's privacy policy for
data handling and account controls. Avoid unnecessary private details in
searches and conversations.
