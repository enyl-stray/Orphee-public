# Early beta 1.28.8

## Verified on these installer bytes

Candidate 28/28, frozen provider/backend-port smoke 46/46 and frozen signup/security smoke 20/20 passed with owned cleanup. Source native-window and UI checks passed. No real-model run was performed on this new hash. The previous 1.28.7 beta separately passed its 24-phase real-model acceptance.

The earlier beta complete suite passed 6,526 tests. These new changes passed 902 pre-commit tests and 127 account/installer tests, not a new complete suite.

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
