# Public onboarding bundles

v1 contains the three standalone examples per language from merged SDK repairs:
- TypeScript: 5f85437b252103b600d3be8fd2bc081e6dca8e56, examples/standalone
- Python: 6159ddb42930cbfa79f1c46cf6e246b5e27d381b, examples

Both require published SDK 1.0.4. JSON is a supported Mintlify static asset on all plans; Python source is transported as data and extracted into fixed filenames by the guide.

Keep v1 unchanged after publication. Publish a new version directory for changes, verify clean npm/venv installs and anonymous HTTP downloads, then update both onboarding guides. Do not copy credentials, internal notes, or unrelated repository files into bundles. Offline success does not satisfy live UO-4 acceptance.
