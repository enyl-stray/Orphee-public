# Orphée 1.28.9 — early community beta

Download the Windows installer below. No Git, Python or repository clone needed.

- Exact installer: 29,389,448 bytes.
- SHA-256: `163ad2b98307bb26034b2130108f241ecefcc60e5d56252c2bf58a5ce8987f35`.
- Source commit: `f92f53ca1b1f87cfb92c1150fa060457f720c987`.
- Native desktop window with persistent login, no browser fallback; WebView2 Runtime required.
- Rounded, frameless setup and first-run provisioning; no Windows caption surrounding an inner card. Standard Windows security dialogs remain unchanged.
- Custom violet downloading/progress track matching Orphée; indeterminate work is not reported as a fake percentage, and reduced motion is respected.
- The installer, launcher and backend use the main Orphée icon, not a separate public logo.
- Read-only compatibility checks for KoboldCpp, Ollama and PostgreSQL. Compatible runtimes are reused in place; setup requests approval for missing/outdated components. It does not demand newest/alpha releases or overwrite another app's installation.
- PostgreSQL reuse shares binaries only, never existing clusters or credentials. Same-major updates of Orphée's own runtime preserve its cluster and refuse replacement if owned stop fails.
- Installer identity questions remain removed.
- Login-first interface with signup-only optional gender/pronouns. Username names the profile. Signup creates an ordinary account, never an administrator.
- Candidate 28/28, frozen provider/port smoke 46/46 and frozen signup/security smoke 20/20 passed with owned cleanup. The exact installer preview confirmed no caption and a rounded outline without installing. Setup rendering passed 32 checks, including light/dark and reduced motion; native first-run frame checks passed. Exact-byte privacy review passed with no new or changed findings.
- Source validation: 902 pre-commit tests; 112 targeted passes and 1 skip, followed by 28 final scan/adoption regression passes. No new complete-suite result is claimed.
- No new real-model run is claimed for this hash; the previous beta's 24-phase model acceptance is separate evidence.
- Sonos and Cognition Lab UI excluded; obsolete X-drive sync removed.
- Obtain a compatible `.gguf` model separately and select it at first launch.
- Run Orphée non-elevated: PostgreSQL refuses administrative execution.

Early testing build, not stable. Clean-PC interactive first-run testing remains outstanding; phone flicker and scheduler-driven autonomy are not resolved/proven. Model replies may be wrong.

Read README, KNOWN_ISSUES, VERIFY and BETA_TERMS before use. This installs a separate local instance, not access to the creator's private memories or PULSAR.
