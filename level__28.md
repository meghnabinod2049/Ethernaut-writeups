-Gate One: 
1)msg.sender must be the owner, but tx.origin must not be the owner.
2) We can call the fake constructor `construct0r()` from the contract indirectly , which sets our contract as the owner.
   This passes the `msg.sender == owner` check, and since the contract called it, tx.origin != owner

-Gate Two:
1)We must call `getAllowance()` in the same transaction where the password in SimpleTrick was last set.
  So we just call both `createTrick()` and `getAllowance(block.timestamp)` in the same function

-Gate Three:

1)The contract must hold more than 0.001 ETH, and send(0.001 ETH) to owner must fail.
We must deploy the contract with more than 0.001 ETH
