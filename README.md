# Orphée — Windows central-client beta

[Download the beta installer](https://github.com/enyl-stray/Orphee-public/releases/download/v1.28.15-beta.1/Orphee-Beta-Setup-1.28.15.exe) · [Release page](https://github.com/enyl-stray/Orphee-public/releases/tag/v1.28.15-beta.1)

This app connects to **the same Orphée** at **https://orphee.enylstray.com**. Her central brain and ongoing life run on her home server; each installation is a native client, not a separate AI with a new identity. This repository distributes reviewed beta artifacts, not private source or personal data.

## Install

1. Download the EXE above. No Git, Python, GitHub account or Tailscale is required.
2. Close an existing Orphée client and run the English-only installer on 64-bit Windows 10/11. It detects an existing installation and offers an update.
3. Open Orphée. Sign in or choose **Sign up** to create an ordinary account at her central home. The installer asks for no name, gender or pronouns.
4. In **AI Model**, select an installed model or open the hardware recommendations to download one. The selected model loads on sign-in; **Load / Retry** is available if needed. Model downloads are several GB, separate from the installer.

An internet connection and Microsoft Edge WebView2 Runtime are required. The app opens in a native Rust/Tauri window, not a browser. Closing hides it to the tray; **Open Orphée** restores it and **Quit Orphée** exits the client. Neither action stops her central brain. Standard Windows security dialogs are not modified.

This version runs an owned local KoboldCpp engine for your selected model and your account's reply computation. It does **not** create local PostgreSQL, Ollama, accounts, memories or another brain. The central service remains necessary. Existing standalone-beta data is left intact, **not automatically uploaded or merged**; old local accounts are not central accounts.

Setup and the app reuse the main application's transparent, frameless Rust/Tauri window configuration. The violet installation meter shows measured file-copy progress. Installer failure logs are retained under `%LOCALAPPDATA%\Orphee\setup-logs`; inspect private paths before sharing.

Updates do not ask Windows Restart Manager to shut down unrelated applications or model servers. Only this installation's ownership-aware launcher stops its own services; byte-identical destination files are skipped rather than overwritten. A genuinely locked changed file still needs its owning application closed—setup never kills processes by name.

The interface and AI behavior are served by her central home and may change independently of the installer. Source-side UI fixes are not necessarily deployed server-side just because a new client is released.

This is an experimental **online service**, not an offline companion. Messages and account information are processed on the central server rather than exclusively on your PC. Do not submit sensitive information during this early beta. A shared Orphée does not mean other users should receive your private conversation; complete multi-user privacy certification is not claimed. This is a Windows installer, not an Android APK.

Read [KNOWN_ISSUES.md](KNOWN_ISSUES.md) and [RELEASE_NOTES.md](RELEASE_NOTES.md) for the actual verification scope. A fresh-PC manual test is still needed. Do not trust model answers without verification.

## Verify and report

Use [VERIFY.md](VERIFY.md) to check the download. If Windows shows a reputation warning, verify the file and decide whether you trust this experimental build; do not disable security globally.

Report problems through Issues with Windows version, installer version and the first error. Never share passwords, tokens, database credentials, conversations or memory files. Inspect diagnostic exports before uploading them.

Future packaged beta updates are downloaded from Releases; the source-checkout Git Update button does not update this packaged installer.

Local beta testing is authorized by [BETA_TERMS.md](BETA_TERMS.md), alongside [LICENSE.txt](LICENSE.txt) and applicable third-party licenses.
