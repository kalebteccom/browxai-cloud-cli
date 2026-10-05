# Browxai Cloud CLI

Official binary distribution channel for the Browxai Cloud connector.
The application source is private. This repository does not grant an open-source license.

Current release: v0.1.0. Each release is a set of Linux archives (x86_64 and
aarch64, glibc 2.36 or newer), `install.sh`, `release-manifest.json`, `SHA256SUMS`
and `SHA256SUMS.minisig`. Every archive was built locally and its build is recorded
in `release-manifest.json`.

Launch downloads are Linux-only. macOS archives are held until Developer ID signing
and notarization are available, and Windows is not available. This connector does
not grant desktop permissions or replace browxai's macOS permission-bearing
application.

Install:

```sh
curl --proto '=https' --tlsv1.2 -fsSLO https://github.com/kalebteccom/browxai-cloud-cli/releases/download/v0.1.0/install.sh
less install.sh
sh install.sh
```

The installer needs `minisign` and `curl`. It installs to `~/.browxai/bin` and
does not change your PATH. Then run `browxai-cloud --version`.

This software uses standard TLS and DTLS-SRTP encryption. It is provided as part
of the Browxai Cloud service and may not be used or downloaded in breach of EU or
applicable sanctions and export laws.

- Product and access: https://cloud.browxai.com/
- Software license: https://cloud.browxai.com/legal/license
- Privacy: https://cloud.browxai.com/legal/privacy
- Support: hello@kalebtec.com

Only trust releases from `kalebteccom/browxai-cloud-cli`. Do not run installation
commands sent by strangers. Official installers verify signed checksums using a
pinned public key. Never disable Gatekeeper or SmartScreen to install the connector.

## Release verification key

The official Minisign public key is:

```text
RWSbt/wJa8Y3Jqw233/Ee3IonbeoqxDTBE/3eMR+lqavUo/G3UDTfkC/
```

After downloading a release's `SHA256SUMS` and `SHA256SUMS.minisig`, verify it with:

```sh
minisign -Vm SHA256SUMS -P RWSbt/wJa8Y3Jqw233/Ee3IonbeoqxDTBE/3eMR+lqavUo/G3UDTfkC/
```

Then verify the archive against its entry in that authenticated manifest. The
official installer performs both checks. This public key is not a private signing
key and does not grant macOS permissions.
