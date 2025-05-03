-The vulnerability in this contract is that it sends ETH to the user before updating their balance. This creates an opening for a reentrancy attack. When the recipient is a smart contract, the contract’s fallback function is triggered.

-The malicious contract donates funds to itself in the original contract.

-The attacker then calls withdraw, triggering the ETH transfer.

-In the attacker’s contract’s receive function, it immediately calls withdraw again before the balance is updated, allowing it to withdraw the same funds multiple times.

-This process continues in a loop, allowing the attacker to drain all the funds from the original contract.
