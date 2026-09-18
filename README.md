# Browxai Cloud CLI

Official binary distribution channel for the Browxai Cloud connector.
The application source is private. This repository does not grant an open-source license.

No public CLI release is available yet. Releases appear here only after artifact
verification, third-party notices, and platform signing checks pass. The public
verification key is configured; release artifacts still need to be built and signed.

The macOS beta will use Minisign-verified downloads and an ad-hoc code signature,
not Apple Developer ID signing or notarization. OS security policy may still block
execution. This connector does not grant desktop permissions or replace browxai's
macOS permission-bearing application.

- Product and beta access: https://cloud.browxai.com/
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
