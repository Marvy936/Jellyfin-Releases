# Security

Do not publish credentials, private source details, media metadata, user data,
or diagnostic logs in this repository. GitHub Issues are disabled; report a
suspected security problem privately to the repository owner.

Release installers are currently unsigned. Verify the attached SHA-256 checksum
and back up `%LOCALAPPDATA%\JellyfinLibraryCompanion` before manual installation.
Packaged Windows builds starting with `0.1.2` may perform those checks and create
a verified backup before running an update, but only after explicit user
confirmation. Unattended or background installation is not supported.
