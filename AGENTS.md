# Documentation repo — agent notes

This repo publishes customer-facing Mintlify docs.

## When touching customer-facing docs

Apply this public contract so pages do not regress:

1. Product category: pre-execution control for AI agents.
2. Decision field: public `decision` is `ALLOW | DENY`. REST evaluate is synchronous and never returns `REVIEW`. On the MCP connector path a borderline action can be held for a human; if nobody answers, it is denied. Do not teach `REVIEW` as an evaluate outcome.
3. Coverage: routed proposed actions only. Unconnected paths are not automatic.
4. Enforcement: Sector8 returns the verdict; the app/runtime must honor it before dispatch.
5. Fail-closed: missing, unknown, error, or timeout → do not dispatch.
6. Telemetry / `POST /api/v1/telemetry`: detective/analysis only. Not enforcement.
7. Compliance: support and evidence for review workflows. Not certification.
8. Evidence: fingerprint / policy identifier language. Avoid unsupported crypto-proof claims (`HMAC`, `SHA-256`, “tamper-evident”) on public pages.
9. Public host: `https://sdkapi.sector8.ai`. Do not put staging hosts on public pages.
10. Credentials: issued to the customer environment. Never commit or paste real keys.

For tiny typo or formatting-only edits that do not change claims, skip the full checklist.

## Before opening a customer-facing docs PR

- Use the checklist in `.github/pull_request_template.md` (or mark N/A for typo-only)
- Prefer `npx mint validate` and `npx mint broken-links` when content or links change
- Touch only files needed for the change

## Repo layout

- Customer-facing pages: `guides/`, `api-reference/`
- Nav: `docs.json` (only listed pages are published)
- This file and `.github/` are internal contributor guidance, not Mintlify content
