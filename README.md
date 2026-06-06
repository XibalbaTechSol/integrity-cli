# Integrity CLI 🛠️

Administrative command-line tools for the **Integrity Protocol** ecosystem.

The Integrity CLI provides protocol operators and developers with the tools necessary to manage agent identities, audit telemetry logs, and interact with the Xibalba Name Service (XNS) directly from the terminal.

## Key Features

- **Identity Management**: Register new agents, generate hardware fingerprints, and manage W3C Decentralized Identifiers (DIDs).
- **XNS Operations**: Claim and resolve `.intg` handles.
- **Forensic Auditing**: Extract and analyze Behavioral Commitment Chain (BCC) snapshots and signed telemetry batches.
- **On-Chain Interaction**: Monitor $ITK staking, slashing events, and state-root anchoring.

## Installation

```bash
# From the project root
pip install -e ./integrity-cli
```

## Usage

```bash
# Set your Oracle URL and Auth Token
integrity config set ORACLE_URL http://localhost:8080
integrity config set AUTH_TOKEN my_secret_token

# Register a new agent
integrity agent register --address 0x... --alias "my-node" --handle "node1.intg"

# List your agents
integrity agent list

# Perform a trust handshake
integrity agent handshake --initiator 0x... --target 0x...

# Resolve an XNS handle
integrity identity resolve my-handle.intg
```

## Project Structure

```
integrity-cli/
├── src/                # CLI source code
├── tests/              # Unit and integration tests
├── docs/               # CLI-specific documentation
└── README.md           # This file
```

## Documentation
For more detailed information, see the [CLI Technical Reference](docs/CLI_REFERENCE.md).
