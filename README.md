**Project_Task**: The "Token" smart contract provides the framework for a custom token with the capability to mint and burn tokens. It features public variables storing token details like name and symbol, and a mapping to manage balances for various addresses. The "mint" function facilitates the creation of new tokens, increasing both total supply and recipient balances, while the "burn" function enables token destruction, reducing total supply and sender balances. The contract includes safeguards to ensure that token burning only occurs if the sender's balance is sufficient. It meets the specified requirements and offers a versatile foundation for managing token transactions and balances on a blockchain platform.

## Solutions 

The "Token" smart contract provides the framework for a custom token with the capability to mint and burn tokens. It features public variables storing token details like name and symbol, and a mapping to manage balances for various addresses. The "mint" function facilitates the creation of new tokens, increasing both total supply and recipient balances, while the "burn" function enables token destruction, reducing total supply and sender balances. The contract includes safeguards to ensure that token burning only occurs if the sender's balance is sufficient. It meets the specified requirements and offers a versatile foundation for managing token transactions and balances on a blockchain platform.

The contract begins with essential declarations and requirements. It specifies the license for the contract using the SPDX-License-Identifier comment and sets the Solidity compiler version to 0.8.18 using the pragma directive. The introductory comments outline the key requirements for the contract, emphasizing the creation and management of a custom token. These requirements include storing token details, managing addresses and balances, implementing minting and burning functions, and ensuring that the burning function includes balance-related conditionals.

Contract Overview and Variables: The contract defines a custom token named "Token." It introduces public variables to store critical token details. The tokenName variable holds the name of the token ("hello"), the tokenSymbol variable stores its symbol ("code"), and the totalSupply variable represents the initial total supply of the token, which is set to 0. These variables provide essential metadata about the token and are accessible externally for transparency and querying purposes.

Balances Mapping: The contract employs a mapping named balances to associate Ethereum addresses with corresponding token balances. This mapping enables efficient tracking of ownership and allows users to retrieve their balances. The mapping is declared as public, granting external read access to token balances for specific addresses. This transparency ensures that token holders can verify their holdings.

**Mint Function - Token Creation:**

The mint function facilitates the creation of new tokens, a process commonly referred to as minting. It takes two parameters: _to (recipient's address) and _value (the number of tokens to be minted). The function starts by requiring that the recipient's address is valid (not the zero address) to prevent accidental token loss. Upon validation, the function increases the totalSupply by the specified _value, effectively adding new tokens to the overall token supply. Simultaneously, it increments the balance of the recipient's address in the balances mapping by the same _value, reflecting the minted tokens in the recipient's account.

**Burn Function - Token Destruction:**

The burn function serves as the counterpart to the mint function, enabling the destruction of tokens. It takes a single parameter: _value (the number of tokens to be burned). To prevent unauthorized token destruction, the function requires that the sender's balance is greater than or equal to _value. If this condition is met, the function decreases the totalSupply by _value, effectively reducing the overall token supply. Additionally, it decreases the sender's token balance in the balances mapping by _value, signifying the burned tokens. This step ensures that the sender's balance accurately reflects the burned tokens.

## Steps To Reproduce 

```
Access Remix IDE: Visit https://remix.ethereum.org/ to use the Remix online IDE.
Create File: Click "New File" on the left sidebar. Name it, like "firstcode.sol," and save with .sol extension.
Write Code: Paste the provided Solidity code into the file. Remix IDE highlights errors and provides real-time feedback. -Compile & Deploy: Use Remix to compile and deploy your contract on Ethereum blockchain. Experience your code in action.
```
