# Security Policy

This is the default security policy for the Scrape.do organisation's public
repositories. A repository with its own `SECURITY.md` is covered by that file
instead; it may name additional scope, versions and timelines.

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues,
discussions or pull requests.**

Report them privately, in either of these ways:

1. **GitHub private vulnerability reporting:** on the repository page, open
   **Security → Report a vulnerability**. This creates a private advisory draft
   visible only to you and the maintainers.
2. **Email:** [security@scrape.do](mailto:security@scrape.do).

Include what the issue is, the steps or a proof of concept to reproduce it, the
affected repository and version, and what you think the impact is. Never
include a real API token or other credential in the report.

You will get an acknowledgement within 3 business days. We will keep you
informed while we investigate and will credit you in the advisory when the fix
is published, unless you prefer otherwise.

## Scope

In scope: the code published in the organisation's repositories, their build
and release pipelines, and the packages they publish (Go modules, npm and PyPI
packages, release binaries).

Out of scope: the Scrape.do service itself (the API, the dashboard and
scrape.do websites), which is reported to
[security@scrape.do](mailto:security@scrape.do) directly rather than through
GitHub; denial-of-service findings that only consume the reporter's own
credits; and findings that require an already-compromised machine.

## Supported versions

Unless a repository says otherwise, security fixes ship in a new release of
the latest minor version; older minors are not patched. Upgrade to the latest
release to receive fixes.
