# Verify the installer

File: `Orphee-Beta-Setup-1.28.10.exe` — **41,688,652 bytes**.

Expected SHA-256:

```text
1b92530852f5f6233501f6dcfcc928b02d8789474b794082d2c0bfbe86900851
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.10.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
