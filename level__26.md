-The CryptoVault uses LegacyToken, which forwards transfer() calls to DoubleEntryPoint.

-When sweepToken() is called with LegacyToken, 
it causes DoubleEntryPoint to transfer DET tokens (wrongly) from the vault to a player

-We should deploy a detection bot that will watch `delegateTransfer()` calls 

Was not able to complete this 
