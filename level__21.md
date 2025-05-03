-The contract calls price() twice, one time to check the price and next to finalize the purchase.

-It should return 101 the first and 0 the second time and price is a view function

-If Shop.isSold() is false it will return 101 and if its true it will return 0

-We can trick the shop as it calls price twice and gets different values
