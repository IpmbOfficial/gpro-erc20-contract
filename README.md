# Gold Pro (GPRO) Token

GoldPro (GPRO) is an ERC20-compliant token designed for seamless transactions, security, and scalability. Built using OpenZeppelin libraries, GPRO supports advanced features such as batch transfers, role-based access control, and the ability to blacklist addresses.

## Overview

- **Token Name:** Gold Pro
- **Symbol:** GPRO
- **Maximum Supply:** 200,000,000 GPRO (200,000 kilograms or 200 tons of 22-carat gold doré bars)
- **Initial Supply:** 3,552,978.71 GPRO
- **Decimals:** 18
- **Blockchain:** Polygon (PoS)
- **Deployment Address:** [0xACe7eb41D6BAd44907cdA84A122F052c74cB7826](https://polygonscan.com/address/0xACe7eb41D6BAd44907cdA84A122F052c74cB7826)

## Features

### Core Features

- **ERC20 Standard:** Fully compliant with the ERC20 token standard.
- **Minting:** Allows approved minters to mint new tokens, up to a maximum supply of 200,000,000.
- **Burning:** Token holders can burn their tokens, reducing the total supply.
- **Batch Transfers:** Simplify sending tokens to multiple addresses in a single transaction.
- **Blacklist:** Restrict specific addresses from making transfers.
- **Pause Functionality:** Pause all token transfers, providing added control during critical events.

### Role-Based Access Control

- **Owner:** Full control over administrative functions.
- **Admin:** Manages minters, authorities, and other admins.
- **Authority:** Adds or removes addresses from the blacklist.
- **Minter:** Can mint new tokens within the predefined limits.

### Security Features

- **Max Supply Enforcement:** Minting is capped at a maximum supply of 200,000,000 tokens.
- **Blacklist Mechanism:** Prevent specific addresses from participating in token transfers.
- **Pause Transfers:** Temporarily disable all token transfers when needed.

## Contract Details

- **Contract Name:** `GoldPro`
- **Compiler Version:** Solidity `^0.8.19`
- **Libraries Used:** OpenZeppelin (v4.9.0)
- **License:** MIT

## Deployment

### Constructor Parameters

The constructor requires the following inputs during deployment:

1. `_name`: The name of the token (e.g., "Gold Pro").
2. `_symbol`: The symbol of the token (e.g., "GPRO").
3. `amount`: Initial supply to be minted and allocated to the deployer's address.

## Functions

### Public and External Functions

#### Core ERC20 Functions

- `transfer(address to, uint256 amount)`: Transfer tokens to a specified address.
- `transferFrom(address from, address to, uint256 amount)`: Transfer tokens on behalf of another address.
- `approve(address spender, uint256 amount)`: Approve another address to spend tokens on behalf of the caller.

#### Administrative Functions

- `addAdmin(address _address, bool _status)`: Add or remove an admin.
- `addMinter(address _address, bool _status)`: Grant or revoke minting permissions.
- `addAuthority(address _address, bool _status)`: Grant or revoke authority permissions.
- `addBlacklist(address _address, bool _status)`: Add or remove an address from the blacklist.
- `pauseStatus(bool _status)`: Enable or disable the paused state.

#### Additional Features

- `batchTransfers(address[] memory _addresses, uint256[] memory _amounts)`: Execute batch transfers.
- `increaseSupply(address _to, uint256 amount)`: Mint new tokens within the maximum supply limit.
- `withdrawERC20(address _contractAddress, address _to)`: Withdraw any ERC20 tokens held by the contract.

## Usage

### Interacting with the Token

Users can interact with the GPRO token using any ERC20-compatible wallet or service. Developers can integrate with the contract using the Ethereum JSON-RPC API.

### Role Management

The owner can assign roles (`Admin`, `Minter`, `Authority`) to other addresses, enabling decentralized governance and efficient management.
