# Design AI releases

This public repository is the binary distribution endpoint for Design AI desktop updates.

- GitHub Releases contain signed and notarized versioned application assets.
- `betas/latest/metadata.json` is the fixed in-app update feed.
- `tests/unsigned/latest/metadata.json` is an isolated, unsigned test-only feed. Production clients must never consume it.
- Source code, local projects, user data, logs, and credentials do not belong here.

The Design AI application verifies the published version, artifact size, and SHA-256 checksum before activating an update. Publishing the latest feed is the final release step and happens only after the immutable version assets pass remote verification.

Unsigned test releases exist only to prove the GitHub download, checksum, activation, relaunch, and local-data-retention path on controlled machines. They are not normal employee distribution builds and never move the production feed.
