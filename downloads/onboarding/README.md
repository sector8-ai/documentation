# Public onboarding bundles

Versioned JSON downloads for the Mintlify onboarding journey. Each file embeds three standalone example scripts for published SDK **1.0.4**.

| Version | Status | Notes |
| --- | --- | --- |
| [v1](./v1/) | Preserved | Initial clean-package path. Do not mutate. |
| [v2](./v2/) | **Current** | Windows `cp1252`-safe console output (ASCII `->` / dashes) so live success exits `0`. |

Source commits:

- TypeScript v2: `31a655a0bacf8a77b72f873684afa71f81d906f2` (`examples/standalone`)
- Python v2: `75b5c0aa56fcab2397f5671ba2f3b64a26d928ed` (`examples`)

Keep published version directories immutable. Add `v3/` (etc.) for further changes, verify clean npm/venv installs and anonymous HTTP downloads, then update both onboarding guides to the new current version while leaving older directories in place.

Do not copy credentials, internal notes, or unrelated repository files into bundles. Offline success does not satisfy live UO-4 acceptance — require exit `0` plus matching Decision Feed evidence with replacement credentials.
