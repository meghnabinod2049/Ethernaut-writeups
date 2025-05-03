-In the Naught Coin smart contract, a key issue arises because the contract only implements the transfer function of the ERC-20 standard, 
while other essential functions (like approve and transferFrom) are inherited from OpenZeppelin’s ERC-20 implementation

-approve: This function allows an address (the "spender") to withdraw tokens from your account up to a specified amount.
transferFrom: This function lets an authorized spender transfer tokens on behalf of the token holder

-First we can verify our balance

-We can approve the contract (player) to transfer the full balance on our behalf

-Use transferFrom to send tokens to another address. 
Since approve grants permission for the contract to withdraw, the transferFrom function allows us to bypass the locked transfer function
