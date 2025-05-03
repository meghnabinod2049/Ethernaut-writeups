- Understood that `tx.origin`  means the external account which initiated the transaction whereas `msg.sender` is the immediate caller of the function

- In case of contract to contract call, the `tx.origin` is not equal to `msg.sender`

- To enable the ownership change, we can deploy an attack contract

`
telephone.changeOwner(_owner);
` 
This is the main logic

-We can pass the our instance address and wallet address to call the changeOwner function

-We can verify the ownership by `await contract.owner()`

-Submit the instance in ethernaut
