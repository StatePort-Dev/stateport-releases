# Release distribution policy

## Versions and channels

Release tags use `v<version>`, where `<version>` follows Semantic Versioning, for example `v1.2.3`. Prereleases use a SemVer suffix, for example `v1.2.3-beta.1`; the same `<version>` (without the leading `v`) appears in asset filenames. A beta or other prerelease is marked **Pre-release** on GitHub and is not a stable release. Platform coverage may differ during prerelease testing; the release notes must say which artifacts are available and any known limits. A stable tag has no prerelease suffix and must not be presented as available before its release assets and checks are ready.

## Release assets

The supported installer names are:

| Platform | Release asset |
| --- | --- |
| macOS Apple silicon | `StatePort-<version>-mac-arm64.dmg` |
| macOS Intel | `StatePort-<version>-mac-x64.dmg` |
| Windows x64 | `StatePort-<version>-win-x64.exe` |
| Linux x86_64 AppImage | `StatePort-<version>-linux-x86_64.AppImage` |
| Linux amd64 Debian package | `StatePort-<version>-linux-amd64.deb` |

Each published release includes `SHA256SUMS` with a SHA-256 entry for **every** installer in that release, using the standard `hash  filename` format. Release notes identify the build, supported platforms, changes, and any relevant installation or update caveats. Installers, checksums, and signatures belong in **GitHub Releases assets**, never in Git history or a repository directory.

## Authenticity and platform checks

Before an artifact is offered as an official download, its published checksum must match the uploaded file. macOS installers are expected to be signed with a StatePort Developer ID and notarized by Apple, with the notarization ticket stapled where applicable. Windows installers are expected to carry a valid StatePort Authenticode signature. Linux AppImage and `.deb` assets are covered by `SHA256SUMS`; a detached signature for `SHA256SUMS` (for example `SHA256SUMS.sig`) should be published with an independently documented verification key when release signing is available. A checksum alone detects corruption but does not establish publisher identity. Do not claim an artifact is signed or notarized unless that specific uploaded artifact has been verified.

A release must not contain placeholder assets, sample checksums, or a tag presented as a downloadable product before real builds are validated. No release is created by this documentation repository's initial setup.
