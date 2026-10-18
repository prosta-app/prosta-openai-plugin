![Prosta](./assets/prosta-icon.svg)

# Prosta for ChatGPT and Codex

Find businesses, compare published services and professionals, and check available
times on Prosta. Connect your existing Prosta account to read your own appointments after explicit consent. Use Uzbek, Russian, or English.

[Prosta](https://www.prosta.app) · [Support](https://www.prosta.app/support) ·
[Connector privacy](./PRIVACY.md) · [Privacy policy](https://www.prosta.app/privacy) ·
[Source](https://github.com/prosta-app/prosta-openai-plugin)

## What it can do

| Capability | Access |
| --- | --- |
| Find businesses and read their public profiles | Public |
| Compare published services and professionals | Public |
| Check available times for eligible services | Public |
| Read your own appointment list and details | Prosta consent for `appointments:read` |

The connector cannot book, cancel, reschedule, take payments, change accounts,
or issue binding quotes. Availability does not reserve a slot. Informational
listings are not necessarily bookable, and unavailable information stays unknown.

## Connect

1. Install this ChatGPT and Codex package using the client's supported plugin controls,
   or add a custom remote MCP connection where your plan and workspace permit.
   Select this repository's package root, keeping all included files and hidden
   configuration files. No local server or dependency installation is required.
2. Use the exact PROD MCP endpoint below. Keep one Prosta
   connection for this endpoint; the endpoint is a protocol service, not a
   browser page. Installation does not configure server credentials.
3. For your appointments, use the host's sign-in flow. Review the Prosta account and `appointments:read` permission before approving. Public discovery works without account consent.

`https://www.prosta.app/api/mcp`

## Try these requests

1. “Find a business on Prosta and show its services.”
2. “Show my upcoming Prosta appointments.”
3. “Show the details of one of my Prosta appointments.”

These are example requests, not a record of completed client acceptance. Use
validated Prosta links returned by tools for the normal booking experience.
Opening a link does not create or change an appointment.

## Account access and privacy

Remove delegated access in [Prosta Connected apps](https://www.prosta.app/connectors/settings), then disconnect the host integration. To switch accounts, revoke the previous connection and sign in explicitly with the intended account. Expired, denied, or failed reads are errors, not empty appointment lists. Revocation prevents future reads; it does not erase information already shared with your host.

The host sends your search terms, selected public business, service and professional
identifiers, and requested availability dates to the configured Prosta server.
If your host supplies a coarse city hint through its
controlled metadata, Prosta may use it for requested nearby discovery. Named
business searches are not automatically restricted to that city. This package does not
ask for GPS coordinates or personal addresses. Hosts without that hint still
support searches by business name or category. With consent, the host receives your own appointment details. Do not include unnecessary private details in searches.

MCP responses use Cache-Control: private, no-store. This does not control
chat-history retention by your AI host. Your host's privacy policy applies to
its conversation; connecting does not change Prosta notification preferences.
Read [Security and privacy](./SECURITY.md) for account and reporting guidance.

## Support and distribution

Contact [Prosta Support](https://www.prosta.app/support) with the integration,
error, and approximate time. Never include passwords, tokens, raw authentication
URLs, or customer records in a public issue or chat.

This bundle runs no local programs and contains no credentials or independent
booking backend. The included proprietary LICENSE retains the original notice and adds limited permission to distribute this Prosta 1.0.0 ChatGPT and Codex package through [the Prosta organization repository](https://github.com/prosta-app/prosta-openai-plugin) and OpenAI, and for end users to install and use it. This includes the genuine Prosta logo supplied with this package. It is not an open-source grant or permission to distribute Prosta application source. Source availability does not itself establish marketplace approval or completed host acceptance.
