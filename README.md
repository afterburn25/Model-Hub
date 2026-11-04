# Model Hub — recovered source archives

**Recovery updated 2026-11-03.** The original complete source ZIPs have now been found in the user's ChatGPT file library, materialized, and verified against recorded SHA-256 checksums. This repository still does **not** yet contain the complete extracted application source, so do not describe main as deployable.

## Verified archived sources

| Product | Source archive | Files | SHA-256 |
|---|---|---:|---|
| Model Hub Pro | `Model-Hub-Pro-1.0.79-Core.zip` | 719 | `b896436dea58593f7c5d635619914f9a711f3c853eb8c17077fb6db1e7ee401f` |
| Model Hub Lite | `Model-Hub-Lite-1.1.60-Core.zip` | 2,830 | `1be33acba03b26c7532c3fd600630ae9a8d2f247937a2ce929f0a2fa1941e5a6` |

The two ZIP archives passed `ZipFile.testzip`, and a source-only recovery package was created from these two lineages under `pro/` and `lite/` respectively (3,548 source files, one machine-specific vendor binding file excluded; no ZIP inside ZIP). The package's **own** SHA-256 is `19b10bfb1d4ba374a78c49d4413572813e157df484028874e572d865e1fb331e`.

## Source import procedure

1. Download `Model-Hub-Source-Recovery.zip` from the recovery chat artifact and verify the SHA above.
2. Extract it to a clean local folder on D: and inspect `RECOVERY_README.md` and `SOURCE_RECOVERY_MANIFEST.json`.
3. From that folder on Windows PowerShell, run `./IMPORT_TO_GITHUB.ps1` for a staged preview. After reviewing the source, run the **same** script with `-Push` to commit and push a new `recovery/model-hub-pro-lite-source-20261103` branch to this repository. The script refuses to overwrite an existing unrelated checkout and never pushes to main.
4. Open a draft PR, review third-party licenses, secret scanning and complete application tests. Keep Pro and Lite independent until compatibility is established.

The connected GitHub file-writing interface currently cannot directly stream the source ZIP's bytes into an entire Git tree, so **source import has not yet occurred**. This README is a provenance/recovery checkpoint, not the complete application.

Central audit: [Code_Library recovery report](https://github.com/afterburn25/Code_Library/blob/library/starter-and-model-catalog-20261103/inventory/REPOSITORY_SOURCE_AUDIT_2026-11-03.md).

## Prepared direct Git source import (text/code phase)

An additional code-only source manifest was prepared and independently checked against a local Git checkout:

- `pro/`: **530 text/code files**
- `lite/`: **975 text/code files**
- **1,505 source files total**
- Expected complete code-only Git tree SHA: `2df21c0d8d9ca21e4e3ec518912c17cfbf6cc533`
- Source manifest: `Model-Hub-Code-Git-Tree.jsonl` (created in recovery workspace, **not committed to GitHub**).
- Manifest SHA-256: `2aaf7e83827705c46593ade175715efaaa3538914765b2bbb44ccf8b2a09c539`
- Preliminary offline text-source scan: no common private-key/API-token signatures found.
- **2,043 other files**, mostly images/artwork and binary assets, omitted from this code-only phase and retained in the complete verified release archives.

The code-only tree is **not a runnable complete Model Hub distribution**: verify remaining assets and dependencies before any deployment. Do not substitute an incomplete code-only import for the original full source recovery kits. Keep both products under separate top-level directories.

