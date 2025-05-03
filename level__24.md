-The proxy's pendingAdmin is stored in the same slot as the wallet's owner

-By calling `proposeNewAdmin(player)` we can set our address as the owner

-Now that we are  the owner, call `addToWhitelist(player)`

-Normally, we can only deposit once per multicall.
But we can nest multicalls inside multicall to trick the contract into depositing twice with only one actual ETH payment.
This doubles our internal balance without increasing contract balance

-We can use `execute()` to transfer all the ETH from contract to our wallet

-The proxy’s admin is in the same storage slot as the wallet’s maxBalance.
Now that the contract balance is 0, we can call `setMaxBalance(player)` to become admin
