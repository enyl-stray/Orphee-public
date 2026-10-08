# Orphée 1.28.10 — unified native beta UI

- Installer: **41,688,652 bytes**.
- SHA-256: `1b92530852f5f6233501f6dcfcc928b02d8789474b794082d2c0bfbe86900851`.
- Artifact source: `0887c2a1f66acceeaa83e5de56909cb9c5eab0f0`, clean private UI branch. Claude's committed public-profile fixes are included; his later database work is separate.

## Changes

- App, setup and provisioning have real frameless rounded native windows, not a rounded web card inside a Windows titlebar.
- Setup and dependency installation reuse the actual production startup HTML, animation and violet loading bar. Progress comes from the worker/installation engine; unknown work does not invent percentages. Reduced motion and light/dark appearance are supported.
- English-only setup, no language/identity questions and no Move window button. Drag the title region normally.
- The exact installation registration is checked. Existing installs show an explicit Update prompt and the registered folder. Interactive updates refuse to overwrite when the installed app cannot be safely stopped; accounts/data are kept.
- Music navigation and Spotify login are disabled for community beta testers; personal builds retain them.
- Non-owner System state reads local-PC CPU/RAM/GPU/OS telemetry. Clients without local telemetry report unavailable rather than presenting server hardware as the user's PC.
- Signup gender dropdown: female, male, non-binary, transgender woman and transgender man, with an optional blank choice. Pronouns remain optional. Signup stays ordinary, never admin.
- Compact login/signup cards fit tested viewports. Native sizing accounts for monitor working area and DPI, including taskbars and secondary monitors.
- Model choices show the complete GGUF filename alongside quantization and size. No model weights are bundled; compatible existing runtimes are reused as before.
- The installer contains a standalone native setup shell around a checksum-bound Inno installation engine. This explains the size increase; no Sonos/ffmpeg or model was added.

## Verification

Candidate 28/28, frozen provider/port 46/46 and frozen signup/security 20/20 passed on these exact bytes, with owned cleanup. The exact-byte privacy verdict passed: all 27 previously approved fingerprints are unchanged. The separate setup-shell audit found no private-fact or relationship material.

Native setup/login previews verified absent Windows captions, rounded outlines, working action bridges and login/signup fit. Existing-install detection was observed against a real disposable registration without pressing Update. Setup rendering passed 32 theme/progress/reduced-motion checks; signup fit was checked at four screen sizes.

Source checks: 902 pre-commit tests, 73 combined focused tests and 9 native-bridge regression tests. Later changes are CSS and rebuilt UI only. No new complete-suite or real-model acceptance is claimed for this installer. Standard Windows security dialogs remain standard.

This is still an early beta. Clean-PC interactive dependency/model downloads need manual testing; Windows/WebView2 are platform prerequisites. Phone flicker and scheduler-driven autonomy are not resolved by this Windows release. Read README, KNOWN_ISSUES, VERIFY and BETA_TERMS before installing.
