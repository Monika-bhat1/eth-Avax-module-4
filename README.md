## MyToken Smart Contract
The MyToken smart contract is an Ethereum-based token contract that extends the functionality of the ERC20 token standard. It provides additional features such as burning tokens, pausing and unpausing token transfers, and allowing users to redeem tokens for specific items.

## Features:
## Token Information:

Token Name: MyToken
Token Symbol: MTK

## ERC20 Standard:
The contract adheres to the ERC20 token standard, allowing for basic token functionality like transferring, approving, and querying balances.
 1. Burning Tokens: Users can burn (destroy) their tokens using the ERC20Burnable extension.
 2. Pausing and Unpausing: The contract owner can pause and unpause token transfers using the Pausable extension. Pausing prevents any token transfers, while 
    unpausing allows transfers to resume.
 3. Redeeming Tokens: Users can redeem tokens for specific items using the redeemtokensForItem function. Redeemable items include a Hoodie, Cap, and Backpack.
    Each item has a different redemption cost in tokens. A shipping cost is also added to the redemption amount.
## Access Control:
 The contract uses the Ownable extension to designate the deployer as the contract owner. Only the contract owner can perform certain actions like pausing, unpausing, and minting new tokens.
## Functions:
1. pause(): Pauses token transfers. Only the contract owner can call this function.
2. unpause(): Unpauses token transfers. Only the contract owner can call this function.
3. mint(address to, uint256 amount): Allows the contract owner to mint new tokens and send them to a specified address.
4. redeemtokensForItem(uint256 itemno): Users can redeem tokens for specific items by providing the item number. Tokens are burned, and the item's redemption cost is deducted from the sender's balance.
5. RedeemableItems(): Allows anyone to view the list of redeemable item names.

## Deployment and Compilation: 
Deploy the contract using a Solidity compiler that supports version 0.8.9.After deployment, the contract owner can mint initial tokens and manage the contract's features.
Usage: Users can transfer tokens using standard ERC20 functions.
To redeem an item, users call the redeemtokensForItem function with the desired item number.
The contract owner can pause/unpause token transfers using the pause and unpause functions.
The contract owner can mint new tokens using the mint function.l
