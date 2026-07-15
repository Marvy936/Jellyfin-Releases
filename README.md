# Jellyfin Library Companion Releases

This public repository is the release channel for the Windows installer of
Jellyfin Library Companion. Application source remains private; this repository
contains no source code, configuration, media metadata, credentials, or user
data.

Use the [latest release](https://github.com/Marvy936/Jellyfin-Releases/releases/latest)
to download:

- `JellyfinLibraryCompanionSetup-<version>.exe`
- `JellyfinLibraryCompanionSetup-<version>.exe.sha256`

Verify the EXE against the attached SHA-256 file before installation. The
installer is currently unsigned. Back up
`%LOCALAPPDATA%\JellyfinLibraryCompanion` before installing or uninstalling;
uninstall removes that complete application-data directory.

Versions through `0.1.1` use this repository for update metadata only. Packaged
Windows builds starting with `0.1.2` can download and install an update after an
explicit user confirmation. Before installation, the app requires the exact
version-matched EXE and checksum assets, verifies the declared download size and
SHA-256, and creates a verified local backup. It then closes the app, runs the
installer, and reopens the installed version. There is no unattended or
background installer execution.

## Release provenance

Each release version is built from the matching `v<version>` tag in the private
source repository. Its CI run validates the project/tag version, builds the
Windows installer, and prepares the checksum bundle. An authenticated operator
then re-verifies the bundle hash before publishing it here. Published versions
are immutable and must not be replaced with different content.
