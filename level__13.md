-Gate One: We  should call the contract from another smart contract, not directly from our wallet, to meet the condition msg.sender != tx.origin

-Gate Three: The key should have a pattern like 0x1111111100000000, and the last two bytes should match the last two bytes of our wallet's address

-Gate Two: We can use loop to test different gas values. We can add small increments to the base value

