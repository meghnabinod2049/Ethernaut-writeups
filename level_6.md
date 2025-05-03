-We are tricking the contract into delegating control to another contract via a fallback function. 
The goal is to become the owner by calling a function pwn() — but that function doesn’t exist in the contract we control. 
Instead, it's in another contract, and the fallback function uses delegatecall to execute it in our contract’s storage

-We can send calldata directly in Remix by passing the first 4 bytes of pwn()

-We can verify the ownership by calling the owner() function and it will return the player address
