# Installing Salryn General Merchandise

[Product overview](README.md) · [Downloads](https://github.com/Kirch-Nairu/Salryn-General-Merchandise/releases) · [Support](SUPPORT.md)

## Before you begin

Salryn is a Windows desktop application. The Beta RC1 package targets x64-compatible Windows PCs; a Windows 11 workstation has been used for internal acceptance. Confirm your specific Windows version, available disk space, hardware and license eligibility with Kirjane before onboarding. Administrator approval is required for setup, not routine application launch.

You do not need to install the .NET SDK, Node.js, npm, Inno Setup, or developer tools. The application contains its local runtime dependencies. Setup detects Microsoft Edge WebView2 Runtime and attempts to install it when missing. Internet access may be necessary for that step, even though routine Host operation is offline-ready.

## First installation

1. Open the official [Releases page](https://github.com/Kirch-Nairu/Salryn-General-Merchandise/releases). If no authorized release appears, contact support rather than obtaining installers from another source.
2. Under Assets, download the Windows setup EXE (not the source-code ZIP or TAR archive).
3. Compare its SHA-256 with the checksum published with that exact release. Check the signature and publisher information as described in the release notes. Do not proceed with a mismatch or unexplained Windows security warning; contact support.
4. Run the installer and approve the Windows administrator prompt if authorized. Follow the wizard.
5. Keep internet access available if setup needs to install WebView2.
6. Open **Salryn POS** from the Start menu or desktop shortcut.
7. Complete the initial store setup and product activation with Kirjane's onboarding guidance. Create authorized staff accounts, configure store details and receipt printing, then validate a test transaction before live operation.

## Verify the downloaded file

In PowerShell, from the folder containing the downloaded installer:

```powershell
Get-FileHash .\Salryn-POS-BetaRC1-Setup.exe -Algorithm SHA256
Get-AuthenticodeSignature .\Salryn-POS-BetaRC1-Setup.exe
```

Compare with the exact release's published checksum and signature status. A matching checksum detects differences from the referenced file; it does not replace a trusted digital signature. Do not disable antivirus, SmartScreen or other security controls.

## Updating an existing installation

- Schedule downtime and complete current transactions and shifts.
- Create a verified application backup and keep a separate protected copy before proceeding. Confirm license recovery arrangements with support.
- Close Salryn, download the approved update and confirm that it is appropriate for your current version.
- Follow the supported installer upgrade procedure. Do not manually delete the database, license files, or application data.
- Reopen the application and verify license status, store details, historical records, stock and receipt printing before returning to live transactions.

The installer preserves the local application-data directory on supported upgrade and uninstall; this is not a substitute for backups. Do not use an older release as a database rollback method without support guidance.

## Local data and backups

Salryn stores business data locally in the Windows application-data directory. Use the in-app Backup & Restore workspace to create and verify backups. Restoring a backup replaces the current local database; only authorized personnel should perform a restore after consulting support when live records are involved.

## Hardware and connectivity

Keyboard-wedge barcode scanners and compatible Windows print queues are supported workflows. Test your exact scanner and printer during onboarding. The supported candidate is a Windows Host installation; LAN terminals are not part of the production offering for this candidate.

For assistance, email [salryn.info@gmail.com](mailto:salryn.info@gmail.com).
