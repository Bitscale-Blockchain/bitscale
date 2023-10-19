# InchScale

This README provides an overview of the technical specifications and project structure for developers interested in contributing to this innovative platform.

## Table of Contents

- [1. Core Infrastructure](#1-core-infrastructure)
  - [1.1 On-Chain Contracts](#11-on-chain-contracts)
    - [1.1.1 Rollup Manager Contract](#111-rollup-manager-contract)
    - [1.1.2 Verifier Contract](#112-verifier-contract)
    - [1.1.3 Data Availability Contract](#113-data-availability-contract)
  - [1.2 Off-Chain Virtual Machine](#12-off-chain-virtual-machine)

- [2. Decentralized Network Architecture](#2-decentralized-network-architecture)

- [3. Ethereum ZK Rollup P2P Network Protocol](#3-ethereum-zk-rollup-p2p-network-protocol)

- [4. Protocol Events](#4-protocol-events)

## 1. Core Infrastructure

### 1.1 On-Chain Contracts

#### 1.1.1 Rollup Manager Contract

The Rollup Manager Contract is the heart of the ZK Rollup ecosystem, managing state and interactions. Key features include:

- **User Balances**: A mapping of user Ethereum addresses to their balances within the Rollup.
- **Contract States**: Management of smart contract states.
- **Data Availability Merkle Tree**: Ensuring data availability using a Merkle tree.

#### 1.1.2 Verifier Contract

The Verifier Contract specializes in efficient proof verification and cryptographic proof validation.

- Focuses on cryptographic proof verification and does not store extensive state variables.
- Verifies the validity of zero-knowledge proofs submitted by Rollup operators.

#### 1.1.3 Data Availability Contract

The Data Availability Contract ensures data availability and utilizes a Merkle tree structure.

- Monitors data availability using a Merkle tree.
- Enhances the security and transparency of the Rollup by mitigating data withholding attacks.

### 1.2 Off-Chain Virtual Machine

The execution engine uses zkEVM for transaction processing. Key components include:

- Transaction execution, including validating transactions, executing smart contracts, and updating account balances.
- State management, maintaining off-chain state using zkEVM.
- Batch creation for efficient processing and Merkle root generation.
- Data availability and validation using zero-knowledge proofs.
- Submission to Layer 1 (L1) for final verification and state transition.

## 2. Decentralized Network Architecture

- **Sequencers**: Independent operators that collect and sequence transactions, ensuring adherence to Rollup rules.
- **Executors**: Distributed across the network to execute transactions within batches off-chain.
- **Provers**: Collaborate with Sequencers to generate zero-knowledge proofs for batches of transactions.
- **Validator Network**: A decentralized network for validating transactions and zero-knowledge proofs.
- **Relayer**: Acts as an intermediary between the off-chain ZK Rollup network and Layer 1 (L1) contracts.

## 3. P2P Network Protocol

**Protocol Version: 1.0**

- Network topology involving Sequencers, Executors, Provers, Validators, and Relayers.
- Structured data exchange format.
- Message format with types like "transaction," "proof," and "state_update."

## 4. Protocol Events

A summary of important events within the protocol, including node discovery, transaction broadcasting, proof generation, validation, state updates, data relaying, L1 submission, data availability monitoring, governance, and monitoring.

For detailed technical specifications and code contributions, please refer to the project's codebase. Happy coding!

---
**InchScale Project Team**
[Website](https://www.inchpower.io) | [GitHub](https://github.com/Inchpower-Blockchain) | [Contact Us](mailto:contact@inchpower.io)
