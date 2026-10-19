![Prosta](./assets/prosta-icon.svg)

# Prosta for ChatGPT and Codex — 1.1.2

Discover Prosta businesses, services, professionals and available times, and
read your own current and past appointments with your existing Prosta account.
When the connected server advertises booking actions, prepare a new booking,
change its time, professional, services or notes, or prepare cancellation.
Every change requires your personal review and approval on Prosta. You can
then check the action result and fetch the current appointment status.

The full capability set has eleven tools: five public discovery reads, two
own-appointment reads and four gated proposal/status tools. Use the live catalog
as the source of available capabilities. If an action tool is absent, use the
normal Prosta booking screens; installing this package does not enable it.
There is no separate AI booking account or appointment database.

This repository contains the ChatGPT and Codex integration package. The package itself
does not deploy the service, enable server capabilities, or establish directory
approval. Use only the tools actually available in the connected server.

## Connect your account

Use the normal ChatGPT and Codex OAuth connection flow to
`https://www.prosta.app/api/mcp` and sign in to your existing Prosta account.
Never paste passwords, OTPs, authorization codes, access tokens or ChatGPT and Codex login
credentials into chat. Read [Connector privacy](./PRIVACY.md),
[Security](./SECURITY.md) and [Prosta Terms](https://www.prosta.app/terms).

Appointment reads need appointments:read. When enabled, proposal and status tools
require fresh, explicit consent for both appointments:read and appointments:write.
An old read-only connection does not receive write access automatically. Do not
request write access while action tools are unavailable. When an enabled action
requires it, reconnect and review the permissions on Prosta. Account identity comes from that verified
sign-in, not a matching email in chat or in ChatGPT and Codex. If the wrong account is
connected, revoke and reconnect with the intended account.

## Proposal workflow when enabled

These steps apply only when the connected server advertises the proposal and
status tools. Until then, ChatGPT and Codex should explain that changes are unavailable
and use a validated normal Prosta link; it must not guess another API or request
notes, cancellation reasons or write consent for an unavailable feature.

1. Choose the actual business, services, professional and available local time,
   or select one of your returned appointments.
2. Ask ChatGPT and Codex to prepare one proposal. Preparation does not reserve a slot or
   change a booking. An uncertain retry uses the same request ID and exact input.
3. Personally open the returned Prosta approval page, review the connected
   account, operation, services, professional, local date/time and total, then
   approve or reject. ChatGPT and Codex must not click approval or perform it through an
   API. A chat message, tool confirmation or opened link cannot replace your
   decision on Prosta.
4. Ask ChatGPT and Codex to check the action status. Only a succeeded action with a canonical
   receipt proves that exact change committed. The receipt is a snapshot at
   commit; fetch the current appointment for its latest details. Pending means
   awaiting business confirmation and must not be described as confirmed.

Proposals expire after ten minutes. The server checks availability, price,
ownership and the exact snapshot again at approval. A taken slot or changed
terms require a new proposal and your new review. Existing appointments appear
in normal Prosta screens through their released realtime clients; reconnect
refreshes missed changes. Old chat messages do not update themselves. Fetch
current appointments again to see later cancellations or rescheduling.

Products, packages, deposits, payments and reference photos require normal
Prosta flows. Existing private appointment notes are not exported. For an edit, omit notes to
preserve them, send explicit new text to replace them, or an explicit empty string to clear them
only when you request removal and the live schema permits it. Include
optional new notes or a cancellation reason only when needed, and avoid medical
or other unnecessary private details in chat.

## Read examples

- “Find up to five salons on Prosta and show their public addresses.”
- “Show my current and past Prosta appointments after I connect my Prosta account.”
- “For the Prosta business and service I choose, show available times tomorrow without booking anything.”

These requests use the available discovery, own-appointment and availability
tools. Resolve real returned identifiers and business-local dates; results may
be empty, and errors must be reported accurately. These examples describe
supported requests, not recorded authenticated host tests. Public discovery
does not require appointment access.

## Proposal examples when the tools are available

- “Find a Prosta service and prepare a booking for me to review on Prosta.”
- “Prepare a change to my selected appointment’s professional, services or notes; I will review it on Prosta.”
- “Prepare cancellation of my selected appointment and let me review it before anything changes.”

These conditional examples are not available while booking actions are disabled
and are not claims of completed host acceptance.

## Controls and support

Revoke access in [Prosta Connected apps](https://www.prosta.app/connectors/settings),
then disconnect ChatGPT and Codex. Revocation blocks later private calls but does not undo
a committed booking or delete ChatGPT and Codex's chat history. Use normal booking controls
for later changes and ChatGPT and Codex's controls for its retained conversations.
MCP private, no-store responses do not override host retention.

Contact [Prosta Support](https://www.prosta.app/support) privately with minimal
sanitized diagnostic details. Do not post customer records or credentials in
public issues. The official distribution repository is
[prosta-app/prosta-openai-plugin](https://github.com/prosta-app/prosta-openai-plugin).

The [LICENSE](./LICENSE) preserves the original proprietary notice and adds
limited permission for this exact ChatGPT and Codex 1.1.2 package, named files and genuine
Prosta artwork. It grants no rights to the private monorepo or separate Claude
release. The package contains no local executable, lifecycle hook or secret.
