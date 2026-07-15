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
check-only/manual-install trust boundary: this repository must not introduce
automatic installer download or execution.
