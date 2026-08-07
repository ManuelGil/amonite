# Verify Your Download

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Every official Amonite release includes signed files and checksums that allow you to verify authenticity and integrity before installation.

This guide explains how to verify an official release using the Amonite Release Signing Key.

## Required files

From the release page, download:

- the ISO image (`amonite-<version>-amd64.iso` or `amonite-lite-<version>-amd64.iso`);
- `*.iso.asc`;
- `SHA256SUMS`;
- `SHA256SUMS.asc`.

Optional but useful:

- `release.json`
- `release.json.asc`

Current downloads are listed in [INSTALL.md](INSTALL.md) and on [amonite.org/downloads](https://amonite.org/downloads/).

You also need the official Amonite Release Signing Key from this repository:

```text
security/amonite-signing-key.asc
```

The signing key is maintained separately from individual releases because it represents the long-term identity of the Amonite Project. Import it once; it should remain unchanged across releases.

A new signing key is published only if the current key is revoked, compromised, or intentionally replaced.

## Import the Release Signing Key

```bash
gpg --import security/amonite-signing-key.asc
```

After importing the key, verify that its fingerprint matches the official fingerprint:

```text
0AFF 5507 8845 4862 6087  F84A 5E1E 335B 601F B44B
```

If the fingerprint does not match exactly, **do not continue**.

## Verify the checksum file

```bash
gpg --verify SHA256SUMS.asc SHA256SUMS
```

Expected result:

```text
Good signature from
"Manuel Gil (Official Release Signing Key) <security@amonite.org>"
```

You may also see:

```text
WARNING: This key is not certified with a trusted signature.
```

That warning is normal when you have imported the key but have not yet established personal trust for it. It does **not** indicate that the signature is invalid.

## Verify the installation image checksum

```bash
sha256sum --check SHA256SUMS
```

Expected result for the file you downloaded:

```text
amonite-<version>-<architecture>.iso: OK
```

If checksum verification fails, do not use the ISO. Download the release again and repeat verification.

Published SHA-256 values for current published Alpha releases:

| Image                                | SHA-256                                                            |
| ------------------------------------ | ------------------------------------------------------------------ |
| `amonite-1.0.0-alpha.2-amd64.iso`    | `9511d94b8f35735d2c94d74f8027a26ce9f61b1057637be1d34547575fda19a9` |
| `amonite-lite-1.0.0-alpha-amd64.iso` | `a0b9f7334aae474ac53cc2fb255975cb67c8727c5f409762a3a9ab3702a95691` |

Always prefer verifying against the signed `SHA256SUMS` file from the same release over copying checksums from secondary sources.

## Verify the ISO signature

```bash
gpg --verify \
    amonite-<version>-<architecture>.iso.asc \
    amonite-<version>-<architecture>.iso
```

Expected result:

```text
Good signature from
"Manuel Gil (Official Release Signing Key) <security@amonite.org>"
```

## Verify release metadata (optional)

If you downloaded `release.json` and `release.json.asc`:

```bash
gpg --verify release.json.asc release.json
```

`release.json` identifies the product, edition, version, codename, architecture, and artifact checksums for automation and cross-checking.

## Verification complete

The download is verified when all of the following are true:

- The Release Signing Key fingerprint matches the published fingerprint.
- `SHA256SUMS` has a valid OpenPGP signature.
- The ISO checksum matches the published checksum.
- The ISO has a valid OpenPGP signature.

If any step fails, do **not** install the downloaded image.

After verification, continue with [INSTALL.md](INSTALL.md).

## Official Release Signing Key

```text
Manuel Gil
(Official Release Signing Key)
<security@amonite.org>
```

Fingerprint:

```text
0AFF 5507 8845 4862 6087  F84A 5E1E 335B 601F B44B
```

This key is used exclusively to sign official Amonite releases.

The fingerprint published in this document, on the official website, and in this repository must always be identical.

Key file: [security/amonite-signing-key.asc](security/amonite-signing-key.asc)
