-The vulnerability in this level lies in how the King contract sends ETH to the current king using .transfer() ,which automatically calls the receive() function of the current king

-We can deploy a malicious contract that becomes king and then refuses to accept ETH when transfer() is called on it. In this way no one can become king after the player

-We can deploy using the instance contract address and value greater than the current prize

-We can verify whether we are the king by `await contract._king()` and it will return the address of the exploit contract

-Submit the instance
