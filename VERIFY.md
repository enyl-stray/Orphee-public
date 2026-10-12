# Verify the installer

File: `Orphee-Beta-Setup-1.28.14.exe` — **35,461,075 bytes**.

Expected SHA-256:

```text
3e150fa479f7ce3645e82cfd059c00471631c153d0c90550c10ba552ae529557
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.14.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
