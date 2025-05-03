- As DEX doesn't check if we are swapping between token1 and token, we can use a fake token

- We can deploy a ERC20 token with fake balanceOf() which returns a huge value for our own address and returns 1 for others

- Since the fake token tells Dex that it has only 1 unit and when we swap it, it will give us all the tokens

- By calling swap() function twice we can drain token1 and toekn2
