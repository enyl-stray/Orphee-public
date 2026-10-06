# Verify the installer

File: `Orphee-Beta-Setup-1.28.7.exe` — **22,586,814 bytes**.

Expected SHA-256:

```text
55be6a11c83f0644d16520415b135a07afd5baa269b9f1b5549f1a98d1e88c55
```

In PowerShell in your download folder:

```powershell
Get-FileHash -LiteralPath .\Orphee-Beta-Setup-1.28.7.exe -Algorithm SHA256
```

The hash must match exactly, ignoring letter case. If it differs, do not run the file. A hash match verifies bytes against this release, not that the software is safe or bug-free.
