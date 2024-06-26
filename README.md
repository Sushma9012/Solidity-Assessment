# MyToken

## Description

MyToken is a basic implementation of an ERC-20 token in Solidity. It provides functionality for creating and destroying tokens, as well as the ability to store additional information about the token.

## Requirements

The contract has public variables that store the details about the coin:

- `tokenName`: A string that serves as the name of the token.
- `abbr`: A string which represents the abbreviation of the token.
- `totalSupply`: An unsigned integer which represents the total supply of the token.

The contract has a mapping of addresses to balances:

- `balances`: A mapping that links addresses to their respective token balances.

The contract has a `mint` function that increases the total supply and the balance of the "sender" address by a given value.

- Parameters:
  - `_address`: The address to which the tokens will be minted.
  - `_value`: The amount of tokens to be minted.
- Actions:
  - Increase the `totalSupply` by `_value`.
  - Increase the balance of the `_address` by `_value`.

The contract has a `burn` function that decreases the total supply by subtracting the mint value from the balance value.

- Parameters:
  - `_address`: The address from which the tokens will be burned.
  - `_value`: The amount of tokens to be burned.
- Actions:
  - Check if the balance of the `_address` is greater than or equal to `_value`.
  - If true, decrease the `totalSupply` by `_value`.
  - Decrease the balance of the `_address` by `_value`.

## Deploying the contract

Deploy the `MyToken` contract to a supported Ethereum network.

Once deployed, you can interact with the contract by calling the following functions:

- `mint`: Creates new tokens and assigns them to a specified address.
  - Parameters:
    - `_address`: The address to which the tokens will be minted.
    - `_value`: The amount of tokens to be minted.
- `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.
  - Parameters:
    - `_address`: The address from which the tokens will be burned.
    - `_value`: The amount of tokens to be burned.

## License

This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.
