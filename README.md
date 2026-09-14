# SSDownload updates

Public update distribution for **SSDownload** (application source stays private).

Contents:

- `version.json` - application update feed (`version`, `url`, `sha256`, `notes`).
- `version.json.sig` - Ed25519 signature over the exact `version.json` bytes, verified against the feed public key embedded in the application.
- `update.xml` - Chrome GUpdate manifest for the self-hosted extension (fixed ID `hgndggnlfpnflkmnbddmcnfniamckham`).
- Release assets per version: `SSDownload-<version>-Setup.exe`, `SSDownload-<version>-win64.zip`, `SSDownload-<version>.crx`, `SHA256SUMS`, both update feeds, the feed signature and `update.xml.sha256sums` (the extension checksum row).

The newest published release is **v1.4.21** (2026-09-14). The application reads
`https://github.com/isolmaz/SSDownload-updates/releases/latest/download/version.json`;
the extension policy and the packaged manifest point at
`https://raw.githubusercontent.com/isolmaz/SSDownload-updates/main/update.xml`.

Published by `scripts/prepare-release.ps1 -Publish` in the private source repository. Do not edit by hand.
