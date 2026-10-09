# Verify the installer

File: `Orphee-Beta-Setup-1.28.11.exe` — **41,692,139 bytes**.

Expected SHA-256:

```text
1d7b732ad619bbe6932675aaa01345de4d7820c4b3b74d34a7f627d48c06d083
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.11.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
