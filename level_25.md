- We can use `web3.eth.getStorageAt()` with the EIP-1967 storage slot to find the engine's address

- Using Ether.js and Engine address, we can create a contract object with functions such as `initialize()` and `upgradeToAndCall()`

- We should confirm that `engine.upgrader()` and `horsePower()` is 0

- Calling the `initialize()`, we can be the upgrader of the Engine contract

- We can deploy a self destruct contract

- By calling `upgradeToAndCall()` we can replace the Engine's logic with the self destruct contract

- When the engine is destroyed and the proxy doesn't work, we completed the level.
