# Kata repositories

Versioned catalog of installable Kata desktop applications. This repository
contains metadata and compatibility information only. Installer binaries are
GitHub Release assets.

## Catalog

[`catalog.json`](./catalog.json) uses schema version 1. Consumers select a
release only when the Forge version, release channel, operating system and
architecture all match.

The current Dojo entry is available only on the `preview` channel. There is no
stable Dojo entry yet.

## Security

Every artifact includes its exact size and SHA-256. A client must verify the
checksum before executing an installer. Artifact URLs are restricted to HTTPS
GitHub Release locations.

## Adding a release

1. Build the installer from a clean tagged source revision.
2. Sign the installer for its target platform.
3. Publish it as a GitHub Release asset.
4. Record the exact SHA-256 and byte size in `catalog.json`.
5. Commit the catalog change only after every referenced asset exists.
