-When the Preservation contract calls the LibraryContract, it updates the storage of Preservation instead of LibraryContract due to how delegatecall works. 
The key is that Preservation stores its timeZone1Library address in slot 0, which we can manipulate.

-We deploy the contract with a setTime function that changes the owner variable in Preservation instead of modifying storedTime

-We call setFirstTime in Preservation with the address of our malicious contract, 
which updates the timeZone1Library slot to our contract’s address.

-We call setFirstTime again to run our contract's code, 
which updates the owner variable to the address that started the transaction

-The owner in Preservation is set to our address, completing the exploit.
