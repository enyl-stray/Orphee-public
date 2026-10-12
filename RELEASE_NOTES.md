# Orphée 1.28.14 — one central Orphée

This Windows beta is a native client of **https://orphee.enylstray.com**, not a new independent Orphée. The release's exact hash and size are in VERIFY.md and SHA256SUMS.txt.

Installer: **35,461,075 bytes**. SHA-256: `3e150fa479f7ce3645e82cfd059c00471631c153d0c90550c10ba552ae529557`.
Private source: `7087c87cc96258ca6e9ffc86f0dda67dd806680c`; build `20261012-132134`. Only the non-deploying beta source branch was pushed.

## Changes

- Connects to her central brain and continuing life without Tailscale or local model downloads.
- Uses the main application's transparent, frameless Rust/Tauri window and persistent WebView session.
- Closing hides to the tray. Open restores the client; Quit exits it without shutting down the central service.
- Keeps login controls available when the central interface predates the packaged native controls. Existing server controls take precedence.
- Refuses local model/database provisioning and local owner creation. A failed connection never starts another local brain.
- Leaves old standalone account data intact, without uploading or merging it. Old local credentials are not central credentials.
- Retains English setup, measured copy progress, update detection and ownership-aware legacy cleanup.
- Identifies its health request explicitly and distinguishes access rejection from an unavailable service.

## Verification of these exact bytes

- Candidate/privacy checks: **29/29**, including Sonos exclusion, declared dependencies and unchanged personal packaged installation.
- Source root pre-commit gate: **902 tests, zero failures**, plus targeted central-client and tray regressions. This is not a new full central-server suite.
- Compiled native tray lifecycle was exercised against inert service callbacks, not a real model.
- Exact installed client: **16/16 checks**, covering anonymous central login, same-origin native bridge, login fitting the window, visible window controls, local-provisioning refusal and no local services. Silent uninstall and registration cleanup also passed.
- Bundled UI fixtures were checked separately. The actual central interface comes from PULSAR; publishing this client does not deploy source-side UI/backend fixes there.

An earlier anonymous-render check failed without sufficient diagnostic output; a diagnostic rerun rendered correctly. Its cause remains unestablished, and failed evidence was retained. No claim of authenticated chat, signup, inference, streaming, reconnection, scheduler behavior or complete multi-user privacy certification follows from the anonymous smoke.

The installer is unsigned. Internet and WebView2 are required. A fresh Windows 10/11 PC still needs manual testing. Phone flicker and model factual accuracy remain separate issues. PULSAR, live accounts and the personal packaged installation were not deployed or modified by this release.
