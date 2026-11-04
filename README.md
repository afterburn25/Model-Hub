# Model Hub — recovered source archives

**Recovery updated 2026-11-03.** The original complete source ZIPs have now been found in the user's ChatGPT file library, materialized, and verified against recorded SHA-256 checksums. This repository still does **not** yet contain the complete extracted application source, so do not describe main as deployable.

## Verified archived sources

| Product | Source archive | Files | SHA-256 |
|---|---|---:|---|
| Model Hub Pro | `Model-Hub-Pro-1.0.79-Core.zip` | 719 | `b896436dea58593f7c5d635619914f9a711f3c853eb8c17077fb6db1e7ee401f` |
| Model Hub Lite | `Model-Hub-Lite-1.1.60-Core.zip` | 2,830 | `1be33acba03b26c7532c3fd600630ae9a8d2f247937a2ce929f0a2fa1941e5a6` |

The two ZIP archives passed `ZipFile.testzip`, and a source-only recovery package was created from these two lineages under `pro/` and `lite/` respectively (3,548 source files, one machine-specific vendor binding file excluded; no ZIP inside ZIP). The package's **own** SHA-256 is `dee17f96cfa71469e2ecce4842b273b6bf8cc8ec2ff497acce8f0c8b07c69fe8`.

## Source import procedure

1. Download `Model-Hub-Source-Recovery.zip` from the recovery chat artifact and verify the SHA above.
2. Extract it to a clean local folder on D: and inspect `RECOVERY_README.md` and `SOURCE_RECOVERY_MANIFEST.json`.
3. From that folder on Windows PowerShell, run `./IMPORT_TO_GITHUB.ps1` for a staged preview. After reviewing the source, run the **same** script with `-Push` to commit and push a new `recovery/model-hub-pro-lite-source-20261103` branch to this repository. The script refuses to overwrite an existing unrelated checkout and never pushes to main.
4. Open a draft PR, review third-party licenses, secret scanning and complete application tests. Keep Pro and Lite independent until compatibility is established.

The connected GitHub file-writing interface currently cannot directly stream the source ZIP's bytes into an entire Git tree, so **source import has not yet occurred**. This README is a provenance/recovery checkpoint, not the complete application.

Central audit: [Code_Library recovery report](https://github.com/afterburn25/Code_Library/blob/library/starter-and-model-catalog-20261103/inventory/REPOSITORY_SOURCE_AUDIT_2026-11-03.md).
