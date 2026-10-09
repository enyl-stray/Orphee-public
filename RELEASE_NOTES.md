# Orphée 1.28.11 — startup corners, progress and update diagnostics

- Installer: **41,692,139 bytes**.
- SHA-256: `1d7b732ad619bbe6932675aaa01345de4d7820c4b3b74d34a7f627d48c06d083`.
- Artifact source: `1866783eced438d20ff96e2548f30da2c37dbb95`, clean private UI branch. No production deployment ref was moved.

## Changes

- Windows 11 compositor rounding replaces jagged GDI clipping and removes the outer outline. The startup scene has no conflicting second CSS corner cutout. Older Windows retain the native region fallback.
- Setup, provisioning and app windows share the same native frame and open centered in the monitor's work area.
- The unchanged violet meter fills monotonically left-to-right. Unknown work holds the measured fill rather than sweeping back and forth; database/runtime subtask percentages are mapped into overall preparation progress.
- Updates check for the registered installation's open desktop window before stopping services or replacing files. Close that window and re-run setup; unrelated installations are not stopped.
- Inno engine logs survive failures in `%LOCALAPPDATA%\Orphee\setup-logs`. Code 5 is labelled cancellation/aborted installation, not a diagnosed file error. The original failure's precise cause remains unknown because its log was not saved.
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

Candidate checks, frozen provider/port configuration and silent uninstall passed on these exact bytes. A separate real-engine fresh install followed by update passed all eight checks, retained two logs and removed its registration on uninstall. The exact-byte privacy verdict passed: all 27 previously approved fingerprints are unchanged. The separate setup-shell audit found no private-fact or relationship material.

Native render-only setup checks verified compositor rounding, absence of a GDI region/caption/frame, centered placement, wizard fit and progress holding/completion. The screenshots were inspected. Browser setup rendering passed 32 light/dark, width, progress and reduced-motion checks. Login/signup behavior retains the previous release's validation; no new account/model run is claimed here.

Source checks: 902 pre-commit tests and 59 focused setup/provisioning tests. No new complete-suite or real-model acceptance is claimed for this installer. Standard Windows security dialogs remain standard.

This is still an early beta. Clean-PC interactive dependency/model downloads need manual testing; Windows/WebView2 are platform prerequisites. Phone flicker and scheduler-driven autonomy are not resolved by this Windows release. Read README, KNOWN_ISSUES, VERIFY and BETA_TERMS before installing.
