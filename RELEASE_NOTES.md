# Orphée 1.28.13 — local status, accounts and model settings

Installer: **35,303,376 bytes**.
SHA-256: `8b12ba84bc267c4f18e28a2ecf89fc9459a512d46f1deed6f588a400fce79102`.
Private source: `da49d718671375951168c75368ea9aca785dddd6`. PULSAR was not deployed.

## Changes

- Bundles declared local hardware telemetry dependencies and uses a real CPU sample.
- Removes the duplicate main-app titlebar while keeping login controls.
- Shows the actual profile relationship instead of inventing "loves" from the username.
- Restricts burp sound controls to the verified owner in the personal edition.
- Clearly separates selected and running models, simplifies downloads, and blocks the first-run start action when a provider already has a model.
- Refreshes installation-local account lists and pictures, reads current profiles, and saves account-specific avatars rather than overwriting a shared image.
- Retains the Tauri setup/provisioning style and safe ownership-aware updates. No model or private account data ships.

## Verification of these exact bytes

- Artifact/privacy: **11 checks, zero failures**, candidate acceptance and unchanged approved privacy findings.
- Actual install → update → uninstall: **12/12**, including survival of an unrelated process holding an unchanged DLL.
- Frozen provider/backend-port configuration: **46/46**, with no model, backend or PostgreSQL started.
- Bundled frontend: **22 browser checks**. Native login/signup: **7/7**, using synthetic HTTP.
- Frozen setup renderer opened and cancelled successfully under an isolated profile.
- Compiled telemetry ran with the payload's own native psutil extension and returned CPU, RAM and GPU information; this was not full backend startup.
- Source: **112 targeted tests** and **902 pre-commit tests**, all passing.

No new complete-suite or real-model acceptance is claimed. Full interactive first-run downloads still need clean-PC manual testing, including a retest on the reporter's Windows 10 PC. Phone flicker, factual accuracy and scheduler-driven autonomy retain their documented limitations. The installer is unsigned. PULSAR and the personal packaged installation remain untouched.
