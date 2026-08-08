# Security policy

## Reporting a vulnerability

Email **[info@advizr.ca](mailto:info@advizr.ca)** with the subject line `SECURITY`.

Do not open a public issue, and do not post the details in a pull request or a discussion. Public
disclosure before a fix is out puts client data at risk.

Include what you need to make the report actionable:

- What the issue is and which repo, service, or domain it affects
- Steps to reproduce, or a proof of concept
- What an attacker gets out of it
- Any logs, requests, or screenshots that help

## What happens next

| Stage | Target |
|---|---|
| We acknowledge the report | 3 business days |
| We confirm or dismiss it, with reasoning | 10 business days |
| We ship a fix for a confirmed issue | Severity dependent, and we tell you the target date |

We will keep you updated while the work is open. If you want credit once the fix ships, say so in the
report and we will name you.

## Scope

In scope: any repository in this organization, `advizr.ca`, `docs.advizr.ca`, and the client
platform.

Out of scope: reports generated purely by an automated scanner with no demonstrated impact, missing
security headers with no exploit path, social engineering of our staff or clients, denial of service,
and anything requiring physical access to a device.

## Rules

Test against your own account and your own data. Do not access, modify, or exfiltrate anyone else's
data. Do not degrade a production service. Stop as soon as you have proved the issue and report it.

Work within these rules and we will not pursue any action against you for the research.

## Secrets

If you find a credential of ours exposed anywhere, treat it as a vulnerability and report it the same
way. Do not use it, not even to confirm that it works.
