# Verify the installer

File: `Orphee-Beta-Setup-1.28.15.exe` — **35,482,029 bytes**.

Expected SHA-256:

```text
51fca6cb96a2c602f625154176c39e0a648b723715eb6737d6e9716eb1169d79
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.15.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
