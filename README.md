# Model Hub — source recovery entrypoint

**Status: source recovery pending.** The original GitHub repository was empty at the start of this audit. Development work and compiled source archives were previously produced outside GitHub, but no complete source ZIP is currently available here.

## Historical development lines

- **Model Hub Pro** — recorded release `1.0.79` (August 3, 2026), with a Core ZIP and incremental upgrade package.
- **Model Hub Lite** — recorded release `1.1.60` (August 21, 2026), with a Core ZIP and 1.1.59-to-1.1.60 upgrade.

**Recorded filenames and hashes**:

```text
Model-Hub-Pro-1.0.79-Core.zip
SHA256 b896436dea58593f7c5d635619914f9a711f3c853eb8c17077fb6db1e7ee401f

Model-Hub-Lite-1.1.60-Core.zip
SHA256 1be33acba03b26c7532c3fd600630ae9a8d2f247937a2ce929f0a2fa1941e5a6

Model-Hub-Lite-1.1.59-to-1.1.60-Upgrade.zip
SHA256 e148091aadf23117c8a7963c06531d97926086b74bd5a3a1901f24b64a8aeef9
```

These are historical records, **not a claim that archives have been restored here**.

Potential reusable implementations include: CMS/visual Design Lab, plugins, page composition, theme variants, installer, admin workflows, update/recovery and versioned extensions. Keep Pro and Lite source lineages separate until proven compatible.

## Next recovery actions

1. Search local downloads, former hosting/VPS directories, backup disks and ChatGPT archive files for the named Core ZIPs.
2. Compare recovered SHA-256 to preserved release metadata before extraction.
3. Inspect recovered source archives for secrets, customer data, dependencies, provenance, licensing and nested archives.
4. Restore verified source on a new recovery branch, add functional tests and document actual current version.
5. Copy **only reviewed, reusable components** to [Code_Library](https://github.com/afterburn25/Code_Library). Do not copy Core-owned implementations redundantly.

The central recovery ledger lives in [Code_Library's review branch](https://github.com/afterburn25/Code_Library/blob/library/starter-and-model-catalog-20261103/recovery/SOURCE_RECOVERY_LEDGER_2026-11-03.md).

**Do not overwrite historical source or declare the application deployable based only on this README.**
