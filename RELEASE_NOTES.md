# Orphée 1.28.12 — real Tauri windows and safer updates

- Installer: **35,192,092 bytes**.
- SHA-256: `04849d1fab569b37455fff29d45f08f5a653e24a612d7bc7aa3a387b86368f99`.
- Source: `b8b1370ae69263e575fbe869354d29f8027026f0`, clean private release branch. No PULSAR deployment ref was moved.

## Changes

- Setup, first-launch provisioning and the packaged app now use Rust/Tauri, pinned to the main desktop's framework versions. The renderer compiles the main app's actual transparent, borderless, shadow-free window configuration; it does not approximate that window with WinForms or binary GDI corner masks. Native clipboard/external-link commands and the startup HTML are reused from the main app.
- All three surfaces open centered. CSS rounded edges can composite over the transparent native window rather than exposing opaque square outer corners.
- The purple progress bar retains its appearance and fills left-to-right from real engine/worker progress. Unknown work holds the last measured value. The real fresh-install test observed intermediate percentages and completion.
- The reported Windows 10 log identifies the previous code-5 failure: Restart Manager failed to close three `llama-server.exe` processes and silent setup aborted before copying. Broad Restart Manager shutdown/restart is now disabled. Only ownership-aware Orphée shutdown handles this installation's services.
- Updates skip destination files with an exact matching SHA-256. An unchanged shared DLL is not overwritten while another application uses it. Changed locked files are not forcibly replaced and unrelated applications are never killed by name.
- The renderer's build/profile paths are remapped out of the public binary. Temporary WebView2 cache cleanup retries boundedly after shutdown; a persistently locked temporary cache is reported as retained, not falsely claimed clean or treated as failed provisioning.
- English-only setup, the main icon and existing account/dependency/model selection behavior remain. Sonos, Cognition Lab and music/Spotify are not enabled in this community release. No model or personal account data ships.

## Verification of these exact bytes

- Candidate gate: **28/28**, including community UI exclusions, declared dependencies, secrets/machine-path checks and untouched personal packaged installation. Exact-hash privacy review passes with unchanged approved findings.
- The frozen setup EXE was opened with an isolated profile: Tauri bridge, transparent body and expected wizard verified; cancellation exited without installing. Its embedded renderer was hash-matched to the build output.
- Real engine fresh install → update → uninstall: **12/12 checks**. A disposable unrelated process kept an installed DLL open throughout the update and survived. Intermediate progress, completion, retained logs, correct registration and registration removal were verified.
- Frozen provider/backend-port configuration: **46/46**, with no model/backend/PostgreSQL started, expected refusals, idempotent settings and complete silent uninstall.
- Source checks: **84 targeted regressions** and **902 pre-commit tests**, all passing. Offline UI checks: **32**, including narrow/desktop widths, both themes and reduced motion. Native login/signup preview: **7 checks**, with synthetic HTTP only and no backend/model.

Automated native checks ran on the build host, not the reporter's Windows 10 PC. That machine still needs a manual retest. No new full-suite or real-model acceptance is claimed. Full interactive first-run downloads, phone flicker and scheduler-driven autonomy retain their documented limitations. Standard Windows security dialogs are unchanged; the installer remains unsigned.
