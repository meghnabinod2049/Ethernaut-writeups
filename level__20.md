-We can create a malicious contract with a fallback() that runs an infinite loop to consume all gas

-We can call the setWithdrawPartner() on the Denial contract with the malicious contract address

-Since fallback runs infinitely and uses all the gas, the calls to withdraw() will fail
