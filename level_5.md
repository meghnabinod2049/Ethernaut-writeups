- In Solidity versions before 0.8.0, numbers didn’t throw an error when they went below zero. Instead, they would wrap around to the maximum possible value.

-Suppose the balance is 0, it will subtract and wrap around giving the address a massive token balance

-Use web3 to encode a malicious transfer() call:

  From an empty account,

  To our original account (the one with 20 tokens),

  With an amount of 2**256 - 21.

-By switching back to our original address, we can check the balance by

`
await contract.balanceOf(player)).toString();
` 

-It will show a huge number

-Submit the instance
