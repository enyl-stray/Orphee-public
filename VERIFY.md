# Verify the installer

File: `Orphee-Beta-Setup-1.28.12.exe` — **35,192,092 bytes**.

Expected SHA-256:

```text
04849d1fab569b37455fff29d45f08f5a653e24a612d7bc7aa3a387b86368f99
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.12.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
