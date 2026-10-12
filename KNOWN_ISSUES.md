# Early beta 1.28.14 — central client

## Verified on these installer bytes

Exact-byte release verification results are recorded in RELEASE_NOTES.md. This client release is not a new real-model or server-deployment claim.

The source passed the 902-test root pre-commit gate and targeted regressions. This is not a new complete-suite result for Claude's separately maintained central server.

## Limitations

- This installer is not Authenticode-signed. Windows may display an unknown-publisher or reputation warning; verify its hash and do not disable security globally.

- Internet and the central service at https://orphee.enylstray.com are required. There is no offline brain or local-model fallback. A fresh-PC manual installation test is still needed.
- The reported Windows 10 installation log establishes the code-5 cause: Restart Manager could not close three `llama-server.exe` users of bundled files, and silent setup defaulted to Abort before copying. This release disables that broad application shutdown and skips byte-identical files. A changed file genuinely locked by another application may still require that application to be closed; the installer does not force-kill unrelated processes.
- The native-window pipeline now uses Tauri on both supported Windows versions. The automated native checks ran on the build host, not the reporter's Windows 10 PC; that machine still needs a manual retest.
- This version does not provision local inference or PostgreSQL. Old standalone data and credentials are retained locally, not uploaded or merged; sign into the central service separately.
- Phone animation/flicker remains unresolved; this is the Windows installer, not the APK.
- Model replies can be inaccurate. Do not rely on this early beta for sensitive information or important decisions.
- An anonymous client-launch check does not establish authenticated conversation, signup, streaming, reconnects, multi-user disclosure or scheduler-driven behavior. These remain separate server acceptance checks.
- The interface comes from the server. Server-side profile pictures, local telemetry presentation, behavior and account handling can require a separate server update; this installer does not redeploy PULSAR.
- Packaged installations cannot update by Git pull; download future installers from Releases.
- Closing hides the client in the tray; Quit exits the client, not her central brain. No new local model is started by this client's GUI.

This is not a stable-release claim and does not deploy personal features or PULSAR.

Previously overwritten avatar files cannot be recovered by this update. Existing standalone beta accounts do not automatically become central accounts.
