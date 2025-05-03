- The registerTreasury(uint8) uses inline assembly and it skips Solidity type checks

- We can send more than 1 byte that means a value greater than 255 even though it says uint8

- This will work as the assembly directly write the raw calldata into stroge and also EVM does not care about types.

- We can claim the title by verifying `await contract.claimLedership()`

