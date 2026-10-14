# Early beta 1.28.15 — central client with local compute

## Verified on these installer bytes

Exact-byte verification results and the bounded source-level real-model transport check are recorded in RELEASE_NOTES.md. These are not a complete installed conversation/factual-fidelity acceptance.

The source passed the 902-test root pre-commit gate and targeted regressions. This is not a new complete-suite result for Claude's separately maintained central server.

## Limitations

- This installer is not Authenticode-signed. Windows may display an unknown-publisher or reputation warning; verify its hash and do not disable security globally.

- Internet and the central service at https://orphee.enylstray.com are required. There is no offline brain or local-model fallback. A fresh-PC manual installation test is still needed.
- The reported Windows 10 installation log establishes the code-5 cause: Restart Manager could not close three `llama-server.exe` users of bundled files, and silent setup defaulted to Abort before copying. This release disables that broad application shutdown and skips byte-identical files. A changed file genuinely locked by another application may still require that application to be closed; the installer does not force-kill unrelated processes.
- The native-window pipeline now uses Tauri on both supported Windows versions. The automated native checks ran on the build host, not the reporter's Windows 10 PC; that machine still needs a manual retest.
- Local inference requires a selected compatible GGUF and sufficient hardware. Downloads are several GB. This version does not provision local PostgreSQL or another brain. Old standalone data and credentials are retained locally, not uploaded or merged; sign into the central service separately.
- Phone animation/flicker remains unresolved; this is the Windows installer, not the APK.
- Model replies can be inaccurate. Do not rely on this early beta for sensitive information or important decisions.
- An anonymous client-launch check does not establish authenticated conversation, signup, streaming, reconnects, multi-user disclosure or scheduler-driven behavior. These remain separate server acceptance checks.
- The interface comes from the server. Server-side profile pictures, local telemetry presentation, behavior and account handling can require a separate server update; this installer does not redeploy PULSAR.
- Packaged installations cannot update by Git pull; download future installers from Releases.
- Closing hides the client in the tray and suspends its owned local model; restoring reloads it. Quit exits the client and its owned engine, not her central brain.
- The central life/time-of-day correction remains pending. The phone flicker, factual fidelity and a fresh-PC manual installation are not claimed fixed by this release.

This is not a stable-release claim. The matching scoped central compute/backend patch was deployed separately; no personal model service was restarted.

Previously overwritten avatar files cannot be recovered by this update. Existing standalone beta accounts do not automatically become central accounts.
