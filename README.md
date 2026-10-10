# Orphée — Windows early beta

[Download the beta installer](https://github.com/enyl-stray/Orphee-public/releases/download/v1.28.13-beta.1/Orphee-Beta-Setup-1.28.13.exe) · [Release page](https://github.com/enyl-stray/Orphee-public/releases/tag/v1.28.13-beta.1)

Orphée is an experimental local AI companion. This repository distributes the community beta, not private development source or the creator's personal installation.

## Install

1. Download the EXE above. You do **not** need Git, Python, a GitHub account or a repository clone.
2. Close the installed Orphée window before updating, then run the English-only installer normally on a 64-bit Windows PC. An existing installation is detected and shown as **Update Orphée**; accounts and data are kept. Do not launch Orphée using **Run as administrator**: PostgreSQL refuses elevated execution.
3. Launch Orphée. Setup checks for compatible existing runtimes and reuses them where possible. Review and approve missing or outdated components before downloading pinned replacements. Internet access and substantial free disk space may be needed.
4. Select a compatible local `.gguf` language model when prompted. Obtain the model separately under its own license: **no model weights ship in this installer**. Models may require several gigabytes of disk/RAM/VRAM; not every PC can run every quantization.
5. Orphée opens in its own desktop window, not a browser. Choose **Sign up** from the login page to create an ordinary account. Your username names the profile; gender/pronouns are optional signup fields. The installer asks for none of these. Community signup never grants administrator powers.

The desktop window requires Microsoft Edge WebView2 Runtime. A missing runtime produces an error, not a browser fallback. Setup, first-run provisioning and the app use frameless rounded windows. Setup and provisioning reuse the actual desktop startup animation and violet loading bar, with the main Orphée icon. There is no Windows titlebar around the login card and no "Move window" button. Standard Windows security dialogs are not modified.

Compatibility checks cover KoboldCpp, Ollama and PostgreSQL. Existing third-party installations are not overwritten or stopped. Reusing PostgreSQL means sharing its compatible binaries only: Orphée creates its own database cluster, credentials and port, never adopts your existing databases. Windows/WebView2 are platform prerequisites, not automatically upgraded drivers or frameworks.

Setup, first-launch provisioning and the app use the main Orphée application's real Rust/Tauri transparent, borderless, shadow-free window configuration and open centered. There is no Windows-version-dependent GDI rounded-mask fallback. The violet progress meter fills left-to-right and holds its last measured percentage during work without a percentage. Remaining at 0% before file copying begins is not a simulated download. Installer failure logs are retained under `%LOCALAPPDATA%\Orphee\setup-logs`; inspect them for private paths before sharing.

Updates do not ask Windows Restart Manager to shut down unrelated applications or model servers. Only this installation's ownership-aware launcher stops its own services; byte-identical destination files are skipped rather than overwritten. A genuinely locked changed file still needs its owning application closed—setup never kills processes by name.

Signup has an optional gender dropdown: female, male, non-binary, transgender woman or transgender man; pronouns remain optional. Login/signup layouts are compact and the native window is bounded to the monitor's usable area. Model download choices show the complete GGUF filename, not only its quantization.

This creates **your own separate installation**. It does not access the creator's PULSAR or private accounts/memories. Sonos implementation/UI and the Cognition Lab are excluded from community builds. Music and Spotify login are disabled for beta testers. Non-owner System state displays local-PC telemetry, not the creator's server; clients unable to read local hardware show an unavailable state. This is a Windows installer, not an Android APK.

Read [KNOWN_ISSUES.md](KNOWN_ISSUES.md) before testing. The full interactive first-run download workflow still needs clean-PC manual verification. Keep backups; do not trust model answers without verification.

## Verify and report

Use [VERIFY.md](VERIFY.md) to check the download. If Windows shows a reputation warning, verify the file and decide whether you trust this experimental build; do not disable security globally.

Report problems through Issues with Windows version, GPU/RAM, model filename and the first error. Never share passwords, tokens, database credentials, conversations or memory files. Inspect diagnostic exports before uploading them.

Future packaged beta updates are downloaded from Releases; the source-checkout Git Update button does not update this packaged installer.

Local beta testing is authorized by [BETA_TERMS.md](BETA_TERMS.md), alongside [LICENSE.txt](LICENSE.txt) and applicable third-party licenses.
