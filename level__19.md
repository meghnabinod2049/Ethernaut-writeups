- Using `makeContact()` function we can interact with the contract

- Using `retract()`, the dynamic codex underflows and its length becomes huge

- We need to calculate the index of the codex that maps to storage slot 0 which is where the owner is stored

- We need to format our address as 32 bytes, preserving the 1-byte contact flag at the end

- By calling revise, it overwrites the slot 0 with the crafted address to become the new owner

- We can verify the ownership
