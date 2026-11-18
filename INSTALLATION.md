# Installing Salryn General Merchandise Beta RC1

[Product overview](README.md) · [Release notes](https://github.com/Kirch-Nairu/Salryn-General-Merchandise/releases/tag/v0.1.0-rc1) · [Support](SUPPORT.md)

> **Pilot testing only — unsigned installer (`NotSigned`).** Native clean-install and upgrade acceptance are incomplete. Use an authorized disposable Windows test environment with fictional data. Do not install on a live client workstation. Shared installer and data identity means this package may upgrade or replace an existing Salryn installation; it is not suitable for side-by-side use.

## Download

**[Download Salryn-General-Merchandise-BetaRC1-Setup.exe](https://github.com/Kirch-Nairu/Salryn-General-Merchandise/releases/download/v0.1.0-rc1/Salryn-General-Merchandise-BetaRC1-Setup.exe)**

[Download the SHA-256 checksum file](https://github.com/Kirch-Nairu/Salryn-General-Merchandise/releases/download/v0.1.0-rc1/Salryn-General-Merchandise-BetaRC1-Setup.exe.sha256.txt)

Version: `0.1.0-rc1` · Size: **23,583,715 bytes**

SHA-256: `d2c5274cc4d28f2590755dc891e503973e8824a3faedf63e11227b2036c74eb8`

Use the EXE under release Assets. GitHub-generated source ZIP/TAR archives contain only public documentation and branding assets, not an installer or proprietary application source.

## Requirements

- An authorized disposable Windows x64 test environment. Confirm your Windows version and hardware with support; native clean-install acceptance has not been completed for this candidate.
- Administrator authorization for setup.
- **.NET 10 Desktop Runtime and ASP.NET Core Runtime.** This package is framework-dependent; these runtimes are not bundled. Developer tools such as the .NET SDK, Node.js, npm, and Inno Setup are not required.
- **Microsoft Edge WebView2 Runtime.** Setup attempts to install it when missing; internet access may be required.
- An appropriate test license and onboarding guidance from support. Accounts Receivable / Utang requires its optional licensed Host entitlement.

## Verify before testing

In PowerShell, from the download folder:

```powershell
Get-FileHash .\Salryn-General-Merchandise-BetaRC1-Setup.exe -Algorithm SHA256
(Get-Item .\Salryn-General-Merchandise-BetaRC1-Setup.exe).Length
Get-AuthenticodeSignature .\Salryn-General-Merchandise-BetaRC1-Setup.exe
```

Confirm the hash and byte count above. The expected signature status is **NotSigned**. Publisher metadata is Kirjane Information Technology Services; it is not authenticated by a trusted digital signature. A matching checksum confirms file integrity, not application safety or trusted signing.

Stop on a hash or size mismatch. Do not bypass or disable SmartScreen, antivirus, or organizational security controls. If execution is blocked, contact support.

## Disposable-environment evaluation

1. Review the release notes and open acceptance gates. Arrange an isolated test environment and test licensing with support.
2. Download and verify both assets. Confirm runtime prerequisites.
3. If organizational policy permits this unsigned beta, run setup in the disposable environment with administrator authorization and follow the wizard. Stop if Windows security controls block execution.
4. Keep internet available if WebView2 setup requires it.
5. Launch **Salryn General Merchandise**, complete authorized test activation and initial setup, and use fictional records.
6. Evaluate checkout, inventory, procurement, reports, printing, and backup/restore as applicable. Record failures and contact support; successful local checks do not imply production acceptance.

## Existing installations, backups, and rollback

**Do not use Beta RC1 to upgrade a live client installation.** Shared installer/data identity can replace an existing Salryn installation. Upgrade data/license preservation, migrations, and rollback have not passed native acceptance.

Before any separately authorized future upgrade, schedule downtime, complete current transactions and shifts, create and verify an application backup, keep a separate protected copy, and confirm license recovery and rollback arrangements with support. Do not delete application data or use an older installer as a database rollback method without support guidance.

Use Backup & Restore only in the disposable environment for this pilot. A restore replaces the current local database. Do not import live client databases into the pilot or post backups and license files publicly.

## Open acceptance gates

- Native Windows clean installation and upgrade: **NOT RUN / BLOCKED**.
- Packed installer payload: **not independently extracted or verified**.
- Windows security lab (Issue #91, Gates A/B/C): **NOT RUN / BLOCKED**.
- Independent source review and trusted signing/timestamping: **pending**.
- Mocked browser suite: **FAIL, 30/56 passed**; 15 visual differences and 11 reported inherited selector mismatches, with the inherited classification not independently reconciled.

Provenance regression 35/35, CoreSmoke, and web unit 15/15 are **reported PASS** checks, not native installation acceptance. No BIR certification or production-ready claim is made. LAN terminals and cloud synchronization are not offered for production use in this candidate.

For assistance, contact [salryn.info@gmail.com](mailto:salryn.info@gmail.com). Include the version, Windows edition, and reproduction steps using fictional data; remove sensitive details from screenshots.
