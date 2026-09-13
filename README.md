# SSDownload updates

Public update distribution for **SSDownload** (application source stays private).

Contents:

- `version.json` - application update feed (`version`, `url`, `sha256`, `notes`).
- `version.json.sig` - Ed25519 signature over the exact `version.json` bytes, verified against the feed public key embedded in the application.
- `update.xml` - Chrome GUpdate manifest for the self-hosted extension (fixed ID `hgndggnlfpnflkmnbddmcnfniamckham`).
- `update.xml.sha256sums` - checksum row for the extension package the update manifest points at.
- Release assets per version: `SSDownload-<version>-Setup.exe`, `SSDownload-<version>-win64.zip`, `SSDownload-<version>.crx`, `SHA256SUMS`.

The newest published release is **v1.4.20** (2026-09-13). The application reads
`https://github.com/isolmaz/SSDownload-updates/releases/latest/download/version.json`;
the extension policy and the packaged manifest point at
`https://raw.githubusercontent.com/isolmaz/SSDownload-updates/main/update.xml`.

Published by `scripts/prepare-release.ps1 -Publish` in the private source repository. Do not edit by hand.
