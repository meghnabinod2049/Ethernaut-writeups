-The variables flattening, denomination, and awkwardness are packed into Slot 2. 
The third item in the data array, 
data[2], is stored in Slot 5 as a bytes32 value

-We can access Slot 5 to get the full 32-byte value of data[2] using getStorageAt

-Since the unlock function only needs the first 16 bytes of data[2], we can slice the first 16 bytes from the 32-byte value

-We can pass the 16-byte key to unlock the contract `await contract.unlock(key)`

