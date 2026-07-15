# Release repository instructions

This repository is public and artifact-only. It owns Jellyfin Library Companion
release metadata, installer assets, and checksums; it does not own application
source code or application documentation.

Never add source code, secrets, tokens, user configuration, media paths,
personal data, logs, reports, or build intermediates. A release must contain
exactly one version-matched Windows installer and its `.sha256` file from the
approved private-source tag CI bundle. Recompute and compare SHA-256 before
publication. Never overwrite an existing version/tag with different content.

The installer is unsigned until Authenticode evidence says otherwise. Keep the
explicit user-confirmation trust boundary: never introduce unattended or
background installer execution. Packaged Windows builds may download and run
the exact version-matched installer only after the user confirms the update,
the declared size and SHA-256 checksum pass, and a verified local backup is
created.
