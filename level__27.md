- GoodSamaritan.requestDonation() tries to donate 10 coins.
If the donation fails with a NotEnoughBalance() error,
it calls wallet.transferRemainder() to send everything left

-The wallet sends coins using a Coin contract.

-If the recipient is a contract, it calls `notify(amount)` on the recipient.

-We can be the contract and inside `notify`, if amount == 10, we revert with a fake NotEnoughBalance() error
