# Early beta 1.28.7

## Verified on these installer bytes

Static/frozen checks passed. Real Stheno-model acceptance passed 24/24 phases, exit 0, with owned cleanup: conversation, source-backed memory, Library/PostgreSQL identity/provenance parity, clearing, restart, correlated retrieval and correct-name reply.

Complete suite before the final harness correction: 6,526 passed, 20 skipped, exit 0. The punctuation correction then passed 159 focused tests and 896 pre-commit tests.

## Limitations

- This installer is not Authenticode-signed. Windows may display an unknown-publisher or reputation warning; verify its hash and do not disable security globally.

- The interactive wizard and full first-run runtime/model workflow still need clean-PC manual testing. The live acceptance used a separately managed local provider.
- Phone animation/flicker remains unresolved; this is the Windows installer, not the APK.
- Correct-name recall passed once, but model replies can be inaccurate. Recall was not isolated from re-injected conversation.
- Forced-cycle state response passed. Scheduler-driven autonomy and causal attribution of all subsystem activity are not proven.
- Do not assume shared personality/memory across accounts or treat this beta as a reviewed sensitive multi-user service.
- Packaged installations cannot update by Git pull; download future installers from Releases.
- No model weights are bundled. Provisioning and model selection need time and disk space.

This is not a stable-release claim and does not deploy personal features or PULSAR.
