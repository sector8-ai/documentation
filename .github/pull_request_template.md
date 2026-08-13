## Summary
<!-- What changed and why -->

## Docs QA checklist

Confirm public pages still match the customer contract:

- [ ] `decision` is `ALLOW | DENY | REVIEW` (do not teach ALLOW/DENY only)
- [ ] Claims apply to **routed** proposed actions only (no automatic coverage of unconnected paths)
- [ ] App/runtime must honor the verdict at dispatch
- [ ] Missing / unknown / error / timeout → fail closed; do not dispatch
- [ ] Telemetry / analyze is detective only; not a substitute for `evaluate`
- [ ] Compliance language is support/evidence, not certification or “makes you compliant”
- [ ] Evidence wording uses fingerprint / policy identifier (no unsupported HMAC/SHA-256/tamper-evident proof claims)
- [ ] Public examples use prod host `https://sdkapi.sector8.ai` only; no staging leakage unless the page is explicitly internal/private onboarding
- [ ] Credentials are “issued to your environment”; do not expose real keys or imply unsupported self-serve key generation

## Test plan
- [ ] `npx mint validate`
- [ ] `npx mint broken-links`
