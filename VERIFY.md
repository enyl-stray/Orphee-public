# Verify the installer

File: `Orphee-Beta-Setup-1.28.8.exe` — **29,088,827 bytes**.

Expected SHA-256:

```text
ef987fdbdda5906960f523114c9352472d07967b2d843a100dc324c9833db28c
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.8.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
