### ERC721 Token Contract README

This ERC721Token.sol contract implements the ERC721 standard for non-fungible tokens (NFTs). It allows the creation, ownership management, and transfer of unique tokens. Additionally, it includes support for safe transfers to prevent accidental loss of tokens and approval mechanisms for third-party operators.

#### Contract Overview

The contract is structured as follows:

- **Library: AddressUtils**: Contains a utility function to determine whether a given address is a contract or not.

- **Interfaces**:
  - `ERC721TokenReceiver`: Defines the interface for contracts to receive ERC721 tokens.
  - `ERC721`: Defines the ERC721 standard interface for NFTs.

- **Contract: ERC721Token**: Implements the ERC721 standard and includes functionalities for token management, ownership, and transfer.

#### Key Functions:

- `mint`: Allows the contract administrator to mint new tokens.

- `balanceOf`, `ownerOf`: Query functions to get the balance of tokens for a given address and the owner of a specific token.

- `safeTransferFrom`, `transferFrom`: Functions to transfer tokens between addresses, with optional data for safe transfers.

- `approve`, `getApproved`, `setApprovalForAll`, `isApprovedForAll`: Functions to manage approval of third-party addresses to transfer tokens on behalf of token owners.

#### Modifiers:

- `canTransfer`: Modifier to ensure that token transfers are authorized by the token owner, approved address, or authorized operator.

#### Frontend

The frontend, built with Drizzle, provides a user interface to interact with the ERC721Token contract. It includes components for viewing token metadata, managing token wallets, and performing administrative tasks.

### Usage Notes

- Before using the application, ensure to configure Drizzle correctly with the desired blockchain network and the corresponding smart contracts.
- Only the contract administrator can mint new tokens and perform administrative tasks.
- Ensure proper authorization and approval mechanisms are in place before transferring tokens to third-party addresses.

This README provides an overview of the ERC721Token contract and its associated frontend. For detailed instructions on how to use the application, refer to additional documentation or comments within the source code.
