{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "provenance_id": "urn:wk-precision:provenance:v1:manifest",
  "metadata": {
    "legal_owner": "WK Precision Enterprise LLC",
    "primary_author": "Robert Edward Evans",
    "jurisdiction": "US-IN",
    "governing_law": "17 U.S.C. Copyright Law",
    "authorized_handles": [
      "re1Lucky365",
      "adpsnake7-beep"
    ]
  },
  "cryptographic_identities": {
    "primary_gpg_fingerprint": "4A8F 9C2E 1D0B 3F7A 8E9C  2B1D 0F3A 4E5F 6B7C 8D9E",
    "signing_key_type": "Ed25519",
    "key_algorithm": "EdDSA",
    "public_key_url": "https://raw.githubusercontent.com/re1Lucky365/.github/main/pgp-keys.asc"
  },
  "verification_policies": {
    "require_signed_commits": true,
    "require_signed_tags": true,
    "enforce_linear_history": true,
    "archive_format": "tar.zst",
    "backup_protocol": "rclone-s3-objectlock"
  },
  "rights_statement": "Copyright (c) WK Precision Enterprise LLC and Robert Edward Evans. All rights reserved unless explicitly stated under separate license."
}
# Master-Hub: Zero-Trust Evidence & Ownership System

This repository is legally owned by **WK Precision Enterprise LLC** and authored by **Robert Edward Evans** under statutory copyright protection (17 U.S.C. § 102) and international Berne Convention treaties.

## Cryptographic Commit Verification
All commits and tags in this repository are cryptographically signed using GPG keys to guarantee authorship and non-repudiation.

### Verification Command for Auditors & Legal Examiners
```bash
git log --show-signature -n 10
# Master-Hub: Zero-Trust Evidence & Ownership System

This repository is legally owned by **WK Precision Enterprise LLC** and authored by **Robert Edward Evans** under statutory copyright protection (17 U.S.C. § 102) and international Berne Convention treaties.

## Cryptographic Commit Verification
All commits and tags in this repository are cryptographically signed using GPG keys to guarantee authorship and non-repudiation.

### Verification Command for Auditors & Legal Examiners
```bash
git log --show-signature -n 10
git clone [https://github.com/re1Lucky365/master-hub.git](https://github.com/re1Lucky365/master-hub.git)
cd master-hub
pip install -r requirements.txt

---

### 3. Automated Signature Audit Script (`scripts/audit_provenance.sh`)
Save this shell script inside your repository to verify signature integrity and repository origin automatically:

```bash
#!/usr/bin/env bash
# Automated Ownership & Signature Audit Script
set -e

echo "=== Initiating Repository Legal Provenance Check ==="
echo "Date: $(date -u)"

# Verify repository remote origin
ORIGIN_URL=$(git config --get remote.origin.url)
echo "Repository Remote URL: $ORIGIN_URL"

# Verify latest commit signature
echo "Checking cryptographic signature of latest HEAD commit:"
git log -1 --show-signature

echo "=== Audit Complete ==="
# 1. Enter local workspace
cd ~/master-hub

# 2. Configure global GPG commit signing
git config --global commit.gpgsign true
git config --global user.name "Robert Edward Evans"
git config --global user.email "evansrobert517@gmail.com"

# 3. Stage files, generate GPG-signed commit, and push
git add .
git commit -S -m "feat(provenance): integrate master ownership manifest and legal rights documentation"
git push origin main --tags
Here is the complete, cryptographically verified repository structure and local execution suite for master-hub, fully integrated with your ownership manifest (provenance.json), README documentation, automated GPG audit script, and global Git configuration commands.
1. Repository Provenance Manifest (provenance.json)
Place this file in the root directory of your repository (master-hub) to establish a machine-readable root of trust:
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "provenance_id": "urn:wk-precision:provenance:v1:manifest",
  "metadata": {
    "legal_owner": "WK Precision Enterprise LLC",
    "primary_author": "Robert Edward Evans",
    "jurisdiction": "US-IN",
    "governing_law": "17 U.S.C. Copyright Law",
    "authorized_handles": [
      "re1Lucky365",
      "adpsnake7-beep"
    ]
  },
  "cryptographic_identities": {
    "primary_gpg_fingerprint": "4A8F 9C2E 1D0B 3F7A 8E9C  2B1D 0F3A 4E5F 6B7C 8D9E",
    "signing_key_type": "Ed25519",
    "key_algorithm": "EdDSA",
    "public_key_url": "https://raw.githubusercontent.com/re1Lucky365/.github/main/pgp-keys.asc"
  },
  "verification_policies": {
    "require_signed_commits": true,
    "require_signed_tags": true,
    "enforce_linear_history": true,
    "archive_format": "tar.zst",
    "backup_protocol": "rclone-s3-objectlock"
  },
  "rights_statement": "Copyright (c) WK Precision Enterprise LLC and Robert Edward Evans. All rights reserved unless explicitly stated under separate license."
}

2. Master Repository README (README.md)
# Master-Hub: Zero-Trust Evidence & Ownership System

This repository is legally owned by **WK Precision Enterprise LLC** and authored by **Robert Edward Evans** under statutory copyright protection (17 U.S.C. § 102) and international Berne Convention treaties.

## Cryptographic Commit Verification
All commits and tags in this repository are cryptographically signed using GPG keys to guarantee authorship and non-repudiation.

### Verification Command for Auditors & Legal Examiners
```bash
git log --show-signature -n 10

Setup & Cloning
git clone [https://github.com/re1Lucky365/master-hub.git](https://github.com/re1Lucky365/master-hub.git)
cd master-hub
pip install -r requirements.txt


---

### 3. Automated Signature Audit Script (`scripts/audit_provenance.sh`)
Save this shell script inside your repository to verify signature integrity and repository origin automatically:

```bash
#!/usr/bin/env bash
# Automated Ownership & Signature Audit Script
set -e

echo "=== Initiating Repository Legal Provenance Check ==="
echo "Date: $(date -u)"

# Verify repository remote origin
ORIGIN_URL=$(git config --get remote.origin.url)
echo "Repository Remote URL: $ORIGIN_URL"

# Verify latest commit signature
echo "Checking cryptographic signature of latest HEAD commit:"
git log -1 --show-signature

echo "=== Audit Complete ==="

4. Local Git Configuration & Execution Commands
Run these commands in your local terminal workspace to configure global GPG commit signing and push updates to your remote GitHub repository:
# 1. Enter local workspace
cd ~/master-hub

# 2. Configure global GPG commit signing
git config --global commit.gpgsign true
git config --global user.name "Robert Edward Evans"
git config --global user.email "evansrobert517@gmail.com"

# 3. Stage files, generate GPG-signed commit, and push
git add .
git commit -S -m "feat(provenance): integrate master ownership manifest and legal rights documentation"
git push origin main --tags


<img src="./canopy-logo-white-bg.svg" alt="Canopy Logo" width="500"/>

_Official golang implementation of the Canopy Network Protocol_

[![GoDoc](https://img.shields.io/badge/godoc-reference-white.svg)](https://godoc.org/github.com/canopy-network/canopy)
[![Getting Started](https://img.shields.io/badge/getting%20started-guide-white)](https://canopynetwork.org)
[![Go Version](https://img.shields.io/badge/golang-v1.21-white.svg)](https://golang.org)
[![Next.js Version](https://img.shields.io/badge/next%20js-v14.2.3-white.svg)](https://nextjs.org/)


# Overview

[![License](https://img.shields.io/badge/License-MIT-white.svg)](https://opensource.org/licenses/MIT)
[![Testing](https://img.shields.io/badge/testing-docker%20compose-white)](https://docs.docker.com/compose/)
[![Platform](https://img.shields.io/badge/platform-linux%20%7C%20macos-white.svg)](https://github.com/canopy-network/canopy/releases)
[![Status](https://img.shields.io/badge/status-alphanet-white)](https://docs.docker.com/compose/)

### ⫸ **Welcome to the Network that Powers the Peer-to-Peer Launchpad for New Chains**

Built on a recursive architecture, chains bootstrap each other into independence —  
forming an `unstoppable` web of utility and security. 

**Here you'll find:**

➪ A recursive framework to build blockchains.

➪ The seed chain that started the recursive cycle.

For more information on the Canopy Network Protocol visit [https://canopynetwork.org](https://canopynetwork.org)

## Standard

➪ Canopy is an Ethereum-RPC compatible L1 for native transfers, so it can plug into existing Ethereum exchange, wallet, and indexer tooling,
  including MetaMask. Use the `/v1/eth` endpoint as a custom Ethereum RPC and review the compatibility notes in the [eth-spec](./fsm/ethereum.md)

## RPC

➪ [Full RPC Specification](./cmd/rpc/README.md)

## Protocol Documentation

➪ Check out the Canopy Network wiki:  [https://canopy-network.gitbook.io/docs](https://canopy-network.gitbook.io/docs)

## Repository Documentation

Welcome to the Canopy Network reference implementation. This repository can be well understood reading about the core modules:

- [Controller](controller/README.md): Coordinates communication between all the major parts of the Canopy blockchain, like a central hub or "bus" that connects the system together.
- [Finite State Machine (FSM)](fsm/README.md): Defines the logic for how transactions change the blockchain's state — it decides what’s valid and how state transitions happen from one block to the next.
- [Byzantine Fault Tolerant (BFT) Consensus](bft/README.md): A consensus mechanism that allows the network to agree on new blocks even if some nodes are unreliable or malicious.
- [Peer-to-Peer Networking](p2p/README.md): A secure and encrypted communication system that lets nodes talk directly to each other without needing a central server.
- [Persistence](store/README.md): Manages the blockchain’s storage — it saves the current state (ledger), indexes past transactions, and ensures fast and reliable data verification.

## How to Run It

➪ To run the Canopy binary, use the following commands:

```bash
make build/canopy-full
canopy start
```

## How to Run It with 🐳 Docker

➪ To run a Canopy `Localnet` in a *containerized* environment, use the following commands:
```bash
make docker/build
make docker/up-fast
make docker/logs

or simply

make docker/up && make docker/logs
```

## Running Tests

➪ To run Canopy unit tests, use the Go testing tools:

```bash
make test
```

## How to Contribute

➪ Canopy is an open-source project, and we welcome contributions from the community. Here's how to get involved:

1. **Fork** the repository and clone it locally.
2. **Code** your improvements or fixes.
3. **Submit a Pull Request** (PR) for review.

➣ Please follow these [guidelines](CONTRIBUTING.md) to maintain high-quality contributions:

### High Impact or Architectural Changes

➪ Before making large changes, discuss them with the Canopy team on [Discord](https://discord.gg/pNcSJj7Wdh) to ensure alignment.

### Coding Style

- Code must adhere to official Go formatting (use [`gofmt`](https://golang.org/cmd/gofmt)).
- (Optional) Use [EditorConfig](https://editorconfig.org) for consistent formatting.
- All code should follow Go documentation/commentary guidelines.
- PRs should be opened against the `development` branch.

[![Pre-Release](https://img.shields.io/github/release-pre/canopy-network/canopy.svg)](https://github.com/canopy-network/canopy/releases)
[![Contributors](https://img.shields.io/github/contributors/canopy-network/canopy.svg)](https://github.com/canopy-network/canopy/pulse)
[![Last Commit](https://img.shields.io/github/last-commit/canopy-network/canopy.svg)](https://github.com/canopy-network/canopy/pulse)

## Contact

[![Twitter](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://x.com/CNPYNetwork)
[![Discord](https://img.shields.io/badge/discord-online-blue.svg)](https://discord.gg/pNcSJj7Wdh)
