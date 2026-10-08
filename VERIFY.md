# Verify the installer

File: `Orphee-Beta-Setup-1.28.9.exe` — **29,389,448 bytes**.

Expected SHA-256:

```text
163ad2b98307bb26034b2130108f241ecefcc60e5d56252c2bf58a5ce8987f35
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.9.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
