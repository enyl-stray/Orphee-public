# Verify the installer

File: `Orphee-Beta-Setup-1.28.13.exe` — **35,303,376 bytes**.

Expected SHA-256:

```text
8b12ba84bc267c4f18e28a2ecf89fc9459a512d46f1deed6f588a400fce79102
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.13.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
