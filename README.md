# nxconvert patched build

This fork fixes NSP conversion crashes caused by a divide-by-zero in progress calculation.

Changes:
- Initialize NSP progress total bytes before decrypting NCAs.
- Guard progress calculations against `total_bytes == 0`.
- Remember the keys path in an external `nxconvert.ini` next to the executable.
- Default the output directory to the selected input file's folder.
- Accept one command-line argument as the input file and prefill the GUI.

Example:

```powershell
nxconvert.exe "H:\NS\Metal Dogs [0100A6E01681C000][v0][JP].nsp"
```

Default `nxconvert.ini` format:

```ini
[Settings]
keys=D:\Citron-Windows-Canary-Refresh_0.6.1\user11\keys\prod.keys
```
