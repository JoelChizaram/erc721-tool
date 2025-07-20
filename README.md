# ERC721 Tool: Flexible NFT Management on Stacks

## Overview

ERC721 Tool is a comprehensive Clarity smart contract suite for managing non-fungible tokens (NFTs) on the Stacks blockchain. This toolkit provides robust, secure, and flexible NFT contract implementations with advanced features for minting, transferring, and managing digital assets.

### Key Features

- Secure NFT minting and transfer mechanisms
- Flexible access control and ownership management
- Support for metadata and token URI management
- Batch minting capabilities
- Role-based access control
- Built-in burn and recovery functions

## Architecture

The ERC721 Tool consists of two primary smart contracts:

- **NFT Registry Contract**: Manages token creation, metadata, and core NFT functions
- **NFT Access Control Contract**: Handles permissions, minting rights, and advanced access management

## Getting Started

### Prerequisites

- Clarinet (latest version)
- Stacks wallet for deployment and testing

### Installation

1. Clone the repository
2. Install dependencies:
```bash
clarinet install
```
3. Run tests:
```bash
clarinet test
```

### Basic Usage

#### Minting an NFT
```clarity
(contract-call? .nft-registry mint-nft 
    tx-sender 
    "https://example.com/token-metadata/1")
```

#### Transferring an NFT
```clarity
(contract-call? .nft-registry transfer 
    token-id 
    tx-sender 
    recipient)
```

## Security Considerations

- Implement proper access control for minting and burning functions
- Use role-based permissions
- Validate token metadata thoroughly
- Implement rate limiting on minting
- Use secure random number generation for unique token IDs

## Development

### Testing
```bash
clarinet test
```

### Local Development
```bash
clarinet start
clarinet deploy
clarinet console
```

## License

MIT License