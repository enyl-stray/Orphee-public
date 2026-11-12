# Orphée 1.28.16 — refreshed Windows beta

This refresh retains one central Orphée, account-bound local reply computation,
the frameless native window and the tray lifecycle.

- Refreshes the packaged client from current source while preserving beta-native
  setup and account-bound compute support.
- Binds local token counting and generation to the same owned model session.
- Rebuilds the community interface independently and excludes development test
  fixtures from package inputs.
- Preserves the central-home connection, local-provisioning refusal and
  ownership-aware close, restore and Quit behavior.
- Updating from 1.28.15 preserved synthetic local data and installed every file
  of the new payload with matching hashes.

The interface and ongoing behavior come from the central home. Publishing this
installer does not deploy source-side prompt or server changes there.

## Exact installer

- File: `Orphee-Beta-Setup-1.28.16.exe`
- Size: **36,081,264 bytes**
- SHA-256: `319766be8cc075bdf6304a281349d62d193dcb7a7e7fd1078d64800b8210d4df`
- Source: `46d4b55d5981f1c5c4a18ffc12075b32cc45e054`
- Build: `20261112-144632`

## Verification and limits

The exact artifact gate passed **29/29** checks. The installed anonymous native
client passed **16/16**, and the disposable **1.28.15 → 1.28.16** upgrade passed
**12/12**, including data preservation, exact payload hashes and owned cleanup.
The exact-artifact privacy review passed with no new or changed unreviewed
constants. Phone/desktop, light/dark and reduced-motion browser checks passed;
the compiled native lifecycle was also exercised with inert service callbacks.

This remains an **experimental prerelease**. Real-model inference, authenticated
conversation, signup, streaming and complete life/memory acceptance were not run
on this installer. Automated installation and upgrade checks used the build host
and synthetic data; fresh-PC and Windows 10 manual testing remain outstanding.
No complete multi-user privacy or real-device performance certification is claimed.

The installer is unsigned. Internet and WebView2 are required; model downloads
are separate. No private source, account data, credentials or raw test evidence
is included in this public release.


## Previous release: Orphée 1.28.15 — local GPU, one shared Orphée

- Selected installed model loads after sign-in; explicit Load / Retry and loaded state come first in AI Model settings. Hardware/download recommendations are secondary.
- Account/device-bound outbound compute uses your local engine while accounts, memory, identity and life stay central. No local PostgreSQL or separate brain.
- Logout resets model context; tray and Quit stop only the client's OS-owned engine.
- Backend deployment now pauses new work, lets admitted tasks finish, and resumes after a backend-only restart. The client reconnects without unnecessarily reloading its selected model.

Installer: **35,482,029 bytes**. SHA-256: `51fca6cb96a2c602f625154176c39e0a648b723715eb6737d6e9716eb1169d79`.
Native source: `d699808e3542c9c645e8b6f4ff8d57908063c7ee`; build `20261014-165216`.
Matching central source: `e04b2a9c04c3dbf9153ab593d12809565e4615e1`, deployed and health checked. KoboldCpp and Ollama service identities stayed unchanged.

Validation: 902 native and 914 server pre-commit tests, focused account/ownership/metadata tests, browser component and reconnect checks, 11 artifact/privacy checks, and the compiled desktop API through the exact bundled Tauri renderer. The real Stheno source-level transport check and owned cleanup passed in 15.1 seconds. This is not a complete frozen-installer conversation/memory/fidelity acceptance or fresh-PC manual test. Life/time-of-day remains pending. No private source or account data is published here.

## Previous release: 1.28.14 — one central Orphée

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
