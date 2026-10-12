# Delimixx — downloads and support

Delimixx is a CSV / TSV editor for Windows that keeps your files as they are: open a file, save it without editing, and you get the same bytes back (with the default save settings). Encoding, line endings and the final newline stay as they were; colors and column widths live in a separate sidecar file, never inside your CSV.

This repository holds the **releases** (signed Windows builds with SHA-256 checksums) and the **public issue tracker**. The source code is not published here.

- Website: https://delimixx.com
- Download page, with verification steps: https://delimixx.com/en/download/
- Changelog: https://delimixx.com/en/changelog/
- Error codes: https://delimixx.com/en/errors/

## Download

Get the latest ZIP from [Releases](../../releases/latest). Requirements: Windows 11, 64-bit. macOS, Linux and Windows 10 are not supported.

1. Extract **the whole folder** (keep `delimixx.exe`, the DLL files and the `lang` folder together).
2. Run `delimixx.exe`. There is nothing to install and no account to create.

### Verify your download

Each release lists the SHA-256 of the ZIP. In PowerShell:

```powershell
Get-FileHash .\delimixx-<version>-prototype-win64.zip -Algorithm SHA256
```

`delimixx.exe` is code-signed (certificate issued by Certum). Right-click it, choose *Properties > Digital Signatures*, and check that the signature is valid and has a timestamp. Windows SmartScreen may still warn about a new publisher; if the checksum and the signature match, choose *More info > Run anyway*.

## What you get in the free build

- Byte-for-byte saving of files you did not edit (with *Save format* on, the default, and the default quote settings); encoding, BOM, line endings and final newline kept after edits.
- UTF-8, UTF-16, Shift-JIS, EUC-JP, JIS, GBK, GB18030, Big5 and EUC-KR, with automatic detection of the encoding and the delimiter.
- Sidecar file (`.cvdeco`) for colors and widths, so your CSV holds only your data.
- A backup before each overwrite (on by default); structure check for rows with the wrong number of columns; detection of external changes.
- Grid editing, undo / redo, find and replace, sort, filter, split view, command palette, keyboard customization, light and dark themes. English and Japanese interface.

No telemetry. The update check is off by default.

## Getting help

- **Something looks wrong or the app crashed:** open an issue with the *Bug report* template. Include *Settings > App Information > Copy Environment Info* (it contains no personal data) and the error code if there is one. **Do not paste private data.** Issues here are public.
- **A question or an idea:** use [Discussions](../../discussions). Issues are for bug reports only.
- **Orders and licenses:** write to support@delimixx.com (not here). **Privacy requests:** write to privacy@delimixx.com. **Refunds:** request them through Paddle (see the Refund Policy on delimixx.com); support@delimixx.com can point you to the right page.
- **A security problem:** do not open an issue. Use *Security > Report a vulnerability* in this repository, or write to security@delimixx.com. See [SECURITY.md](SECURITY.md).

You can write in English or Japanese.

## License

The Delimixx software is proprietary; see the Terms of Use at https://delimixx.com/en/terms/. Open-source components are listed in `THIRD-PARTY-NOTICES.txt` (inside every download) and at https://delimixx.com/en/licenses/.

© Quintastella
