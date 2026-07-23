# Verify Your Download

Every official Amonite release includes signed files and checksums that allow
you to verify its authenticity and integrity before installation.

This guide explains how to verify an official release using the Amonite Release
Signing Key.

## Required Files

From the release directory, download the following files:

- `amonite-<version>-<architecture>.iso`
- `amonite-<version>-<architecture>.iso.asc`
- `SHA256SUMS`
- `SHA256SUMS.asc`

You also need the official Amonite Release Signing Key.

The public signing key is available from:

```
security/amonite-signing-key.asc
```

The signing key is maintained separately from individual releases because it
represents the long-term identity of the Amonite Project. You normally need to
import it only once, and it should remain unchanged across releases.

A new signing key is published only if the current key is revoked, compromised
or intentionally replaced.

## Import the Release Signing Key

Import the official public key.

```bash
gpg --import security/amonite-signing-key.asc
```

After importing the key, verify that its fingerprint matches the official
fingerprint published by the Amonite Project.

```
0AFF 5507 8845 4862 6087  F84A 5E1E 335B 601F B44B
```

If the fingerprint does not match exactly, **do not continue**.

## Verify the Checksum File

Verify that the checksum file has been signed with the official Release Signing
Key.

```bash
gpg --verify SHA256SUMS.asc SHA256SUMS
```

Expected output:

```
Good signature from
"Manuel Gil (Official Release Signing Key) <security@amonite.org>"
```

You may also see a message similar to:

```
WARNING: This key is not certified with a trusted signature.
```

This warning is normal when you have imported the key but have not yet
established personal trust for it. It does **not** indicate that the signature
is invalid.

## Verify the Installation Image

Verify that the downloaded ISO matches the published checksum.

```bash
sha256sum --check SHA256SUMS
```

Expected output:

```
amonite-<version>-<architecture>.iso: OK
```

If the checksum verification fails, do not use the ISO. Download the release
again and repeat the verification steps.

## Verify the ISO Signature

Verify that the installation image itself was signed using the official
Release Signing Key.

```bash
gpg --verify \
    amonite-<version>-<architecture>.iso.asc \
    amonite-<version>-<architecture>.iso
```

Expected output:

```
Good signature from
"Manuel Gil (Official Release Signing Key) <security@amonite.org>"
```

## Verification Complete

The download is verified when all of the following conditions are met:

- The Release Signing Key fingerprint matches the published fingerprint.
- `SHA256SUMS` has a valid OpenPGP signature.
- The ISO checksum matches the published checksum.
- The ISO has a valid OpenPGP signature.

If any verification step fails, do **not** install the downloaded image.

## Official Release Signing Key

```
Manuel Gil
(Official Release Signing Key)
<security@amonite.org>
```

Fingerprint:

```
0AFF 5507 8845 4862 6087  F84A 5E1E 335B 601F B44B
```

This key is used exclusively to sign official Amonite releases.

The fingerprint published in this document, on the official website, and in the
repository must always be identical.
