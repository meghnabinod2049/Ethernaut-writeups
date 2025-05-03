-The flipSwitch has a guard that check if we are calling `turnSwitchOff()` by checking the raw data at byte 68

-We can make custome input such that it pretends to call the `turnSwitchOff()` at byte. This is to fool the guard.

-It actually calls the turnSwitchOn() from the real data stored later in the input

-The `await contract.switchOn()` returns true
