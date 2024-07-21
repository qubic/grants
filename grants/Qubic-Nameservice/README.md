# Qubic Name Service (QNS)

## Overview

Welcome to the Qubic Name Service (QNS) project. This document provides a high-level design and specification of a decentralized domain name system for Qubic. The goal is to simplify blockchain interactions by converting complex Qubic addresses into human-readable names. This will enable users to register usernames, such as `name.qubic`, instead of using traditional addresses.

## Objectives

The primary objectives of QNS are:
- Simplify user interactions with the blockchain by using human-readable names.
- Enhance user experience and accessibility.
- Facilitate easier and more secure transactions and exchanges.
- Promote the growth of the Qubic network by increasing user volume and engagement.

## High-Level Design

This section outlines the high-level architecture of the Qubic Name Service (QNS). The design focuses on user registration and name resolution, integration with decentralized storage, and ensuring security and privacy.

1. **User Registration and Name Resolution**
    - Users can register unique usernames on the Qubic network.
    - It can be directly integrated into the Qubic wallets.
    - Each username maps to a unique Qubic address.
    - All Smart Contracts of the Qubic network can make calls to the QNS.
    - The system maintains a decentralized registry of these mappings.

2. **Qubic Name Service Protocol**
    - A smart contract will manage the registry of names and addresses.
    - The contract will provide functions for name registration, resolution, and transfer.
    - The protocol will include a method for resolving usernames to their corresponding Qubic addresses.
    - QNS will enable users to create subdomains under their primary domain name, allowing for better organization and management of services. For example, users can have a primary QNS domain for their website, with subdomains for several services or DApps.
    - Users can assign a QNS name to a QFT.
    - QNS can serve as a personal identity system.

3. **Decentralized Storage Integration**
    - Integrate with IPFS (InterPlanetary File System) for decentralized storage of additional user information.
    - Users can associate metadata with their usernames, stored securely on IPFS.

4. **Security and Privacy**
    - Ensure the security of user data through encryption and decentralized storage.
    - Implement mechanisms to prevent name squatting and fraudulent activities.

## Components

This section details the core components of the Qubic Name Service (QNS) system. It includes smart contracts, user interface, and backend services necessary for the seamless functioning of QNS.

1. **Smart Contracts**
    - **Registry Contract**: Manages the registration, resolution, and transfer of usernames.
    - **Resolver Contract**: Provides methods for resolving usernames to Qubic addresses.

2. **User Interface**
    - **Web Interface**: A user-friendly web interface for name registration, management, and lookup.
    - **API**: An API for developers to integrate QNS functionality into their applications.

3. **Backend Services**
    - **Database**: Decentralized storage of usernames and metadata.
    - **Indexer**: A service to index and retrieve user information efficiently.

## Workflow

This section describes the end-to-end workflow for user registration, name resolution, and metadata management in the Qubic Name Service (QNS). The workflow ensures a streamlined process for users interacting with the system.

1. **Registration**
    - User submits a registration request via the web interface or API.
    - Smart contract verifies the availability of the username.
    - Upon successful verification, the username is registered, and the mapping is stored in the registry.

2. **Name Resolution**
    - User or application requests the address associated with a username.
    - Resolver contract retrieves the address from the registry and returns it.

3. **Metadata Management**
    - Users can associate additional information with their usernames.
    - Metadata is stored on IPFS, and the corresponding IPFS hash is linked to the username in the registry.

## Detailed Protocol Design

This section provides a comprehensive description of the registration process, name resolution process, and metadata management process. The detailed protocol design is essential for developers to understand the intricacies of the QNS system.

### 1. Registration Process
- **User Interface**: Users will interact with a web-based registration form or API endpoint.
- **Smart Contract Interaction**: The registration form will initiate a transaction with the Registry Contract.
- **Username Availability Check**: The Registry Contract will check if the desired username is available.
- **Transaction Confirmation**: If available, the username is registered upon transaction confirmation, linking it to the user’s Qubic address.

### 2. Name Resolution Process
- **Lookup Request**: Users or applications will send a lookup request to the Resolver Contract.
- **Registry Query**: The Resolver Contract will query the Registry Contract to retrieve the Qubic address associated with the username.
- **Response**: The Qubic address is returned to the requester.

### 3. Metadata Management Process
- **Metadata Submission**: Users can submit additional information (e.g., profile data) via the web interface or API.
- **IPFS Storage**: The metadata is stored on IPFS, and an IPFS hash is generated.
- **Registry Update**: The IPFS hash is linked to the username in the Registry Contract.

## Security Measures

This section outlines the security measures implemented to protect the QNS system and its users. It includes prevention of name squatting, data encryption, and fraud prevention.

1. **Name Squatting Prevention**
    - Implement mechanisms such as a registration fee and periodic renewal to prevent name squatting.
    - Introduce a dispute resolution process to handle conflicts over name ownership.

2. **Data Encryption**
    - Encrypt sensitive user data before storing it on IPFS.
    - Ensure end-to-end encryption during data transmission.

3. **Fraud Prevention**
    - Implement identity verification processes during registration.
    - Monitor and flag suspicious activities on the network.

## Proposals and Improvements

Improvements to the protocol or changes to this description aimed at enhancing its functionality are also welcome. Proposals that include a technical and functional design have a higher chance of being accepted, along with the consideration of ease of integration.
