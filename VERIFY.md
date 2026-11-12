# Verify the installer

File: `Orphee-Beta-Setup-1.28.16.exe` — **36,081,264 bytes**.

Expected SHA-256:

```text
319766be8cc075bdf6304a281349d62d193dcb7a7e7fd1078d64800b8210d4df
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.16.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
