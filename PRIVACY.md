# Privacy for the Prosta ChatGPT and Codex connector — 1.1.2

This notice describes the Prosta 1.1.2 ChatGPT and Codex integration alongside the
[Prosta privacy policy](https://www.prosta.app/privacy) and
[terms](https://www.prosta.app/terms). It governs the connector-specific sharing
and additional AI-host recipient described here. It does not change the separate
Claude package or the scope of the earlier read-only 1.0.0 package.

The connected server controls which tools are available. Proposal-specific
processing applies only when those tools are enabled and you give the required
fresh consent. This notice does not activate processing or claim authenticated
host testing is complete.

## What is shared and why

Public discovery sends search terms, selected public business, service and
professional identifiers, and availability dates to Prosta. Results include
public profiles, catalogs, professionals and available times. ChatGPT and Codex can supply
an optional coarse city hint through controlled metadata; this integration does
not request GPS coordinates or personal addresses.

With explicit appointments:read consent, your verified Prosta account can read
its own current and past appointments: booking identifiers and status, business
and professional details, services, dates/times, duration and prices. Existing
private appointment notes are excluded. Account identity comes from Prosta
sign-in; a matching host email or email typed in chat does not establish it.
This is your regular Prosta account and history, not a new AI booking account.

When enabled, booking proposal and status tools require fresh explicit consent for both
appointments:read and appointments:write. An existing read-only grant does not
upgrade automatically. Your selected OpenAI host sends a request UUID, operation, business or
appointment ID, selected professional/services, and proposed date and time.
Optional notes or a cancellation reason are only text you explicitly supply for
that request. Those new notes/reason may be included in the proposal returned to
ChatGPT and Codex; old appointment notes are never copied into it or returned. Avoid medical
or other unnecessary private details in notes and conversations.

When you use an enabled preparation tool, Prosta creates an immutable,
account-bound proposal with the exact change and
server-calculated total. Preparation does not reserve or alter an appointment.
You personally review and approve or reject on Prosta with the same account.
The server rechecks consent, ownership, snapshot, price and availability before
the canonical appointment workflow executes. ChatGPT and Codex or a chat confirmation
cannot perform that first-party decision. A successful action returns a minimal
receipt of the appointment at commitment; a fresh appointment read provides the
latest details. A pending appointment is not confirmed.

OpenAI receives the inputs, tool results and text you place in ChatGPT and Codex to
answer your request under its account settings and
[privacy policy](https://openai.com/policies/privacy-policy/). This is an additional
connector-specific recipient alongside the general Prosta policy. ChatGPT and Codex may
retain conversations independently of Prosta. Never paste passwords, OTPs,
authorization codes or access tokens into chat. Installing a package does not
grant account access or approve a booking change.

## Expiry and retained records

Proposals expire after ten minutes. Expiry ends approval eligibility; it does
not physically delete the immutable request, proposal or receipt. These records
remain with consent history until the relevant account or consent record is
deleted. Revoking access blocks later use but does not itself promise to purge
that history. Canonical appointments remain normal Prosta booking records.

Current connector configuration expires access tokens after five minutes,
authorization codes after one minute and unfinished consent interactions after
ten minutes. Refresh credentials and connection sessions have a one-day provider
lifetime. Consent is valid for at most 30 days and may end sooner through
revocation or session expiry. Expired provider records are cleaned in bounded
batches during subsequent provider writes. Expiry is not an immediate physical
deletion promise; no separate logging retention deadline is asserted here.

MCP responses use Cache-Control: private, no-store. This does not erase ChatGPT and Codex
messages or override OpenAI's retention controls. Old chat cards remain
snapshots. Prosta screens depend on their released realtime clients and
connectivity; reconnecting refreshes missed changes.

## Your controls

Remove delegated access in Prosta Profile → Connected apps, then disconnect the
integration in ChatGPT and Codex. This blocks future private calls and removes its token
family; it does not undo a committed booking or erase data already returned to
ChatGPT and Codex. Use regular booking controls for subsequent changes and your host’s
account/conversation controls for retained data. To switch accounts, revoke
the previous connection and sign in with the intended account before consenting.

Prosta account deletion removes connector provider state, consent history and
related proposals/receipts through the account-deletion workflow. This connector
does not support products, packages, deposits, payments or reference photos;
use normal Prosta flows for those requests.

For access, deletion or privacy questions, contact
[Prosta Support](https://www.prosta.app/support) privately. Do not include customer
records or credentials in public issues. See [Security](./SECURITY.md) for private
reporting. This notice describes handling; it is not a claim of directory or
independent compliance approval.
