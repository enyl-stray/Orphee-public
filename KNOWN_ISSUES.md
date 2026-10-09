# Early beta 1.28.12

## Verified on these installer bytes

Exact-byte release verification results are recorded in RELEASE_NOTES.md. No real-model run is claimed for this new hash. The previous 1.28.7 beta separately passed its 24-phase real-model acceptance.

The earlier beta complete suite passed 6,526 tests. The installer changes are checked with the 902-test pre-commit gate, targeted regressions, rendering checks and frozen installation tests, not a new complete suite.

## Limitations

- This installer is not Authenticode-signed. Windows may display an unknown-publisher or reputation warning; verify its hash and do not disable security globally.

- The interactive wizard and full first-run runtime/model workflow still need clean-PC manual testing. The live acceptance used a separately managed local provider.
- The reported Windows 10 installation log establishes the code-5 cause: Restart Manager could not close three `llama-server.exe` users of bundled files, and silent setup defaulted to Abort before copying. This release disables that broad application shutdown and skips byte-identical files. A changed file genuinely locked by another application may still require that application to be closed; the installer does not force-kill unrelated processes.
- The native-window pipeline now uses Tauri on both supported Windows versions. The automated native checks ran on the build host, not the reporter's Windows 10 PC; that machine still needs a manual retest.
- Dependency discovery checks configuration, PATH, known installation directories and PostgreSQL installer registration; it is not an exhaustive scan of every disk. Unknown or prerelease versions are not silently reused. The compatible floors are KoboldCpp 1.114.1, Ollama 0.6.0 and PostgreSQL 16.15 within major version 16. An old external runtime is left intact; approved replacements are installed for Orphée.
- Phone animation/flicker remains unresolved; this is the Windows installer, not the APK.
- Correct-name recall passed once, but model replies can be inaccurate. Recall was not isolated from re-injected conversation.
- Forced-cycle state response passed. Scheduler-driven autonomy and causal attribution of all subsystem activity are not proven.
- Do not assume shared personality/memory across accounts or treat this beta as a reviewed sensitive multi-user service.
- Packaged installations cannot update by Git pull; download future installers from Releases.
- No model weights are bundled. Provisioning and model selection need time and disk space.

This is not a stable-release claim and does not deploy personal features or PULSAR.
