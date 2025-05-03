-Solidity’s private keyword only restricts access within other smart contracts, not from outside. 
Since all contract storage is public, we can directly read any variable, even private ones by accessing its storage slot.

-We can read the slot using `await web3.eth.getStorageAt(contractAddress, 1)`

-We will get a password which can be used to unlock the vault 

-We can confirmed whether the vault is unlocked by `await contract.locked(); ` and it should return false

-Submit the instance
