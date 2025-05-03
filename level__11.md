-The Elevator contract assumes that the isLastFloor function in the Building contract will always give the same answer for any given floor.
This is because it’s treated like a pure function, meaning it should just return a value without causing any changes or side effects.

-We can create an attack contract that messes with the isLastFloor function. 
Instead of returning the same result every time, the function alternates between false and true, flipping its answer back and forth.

-When the Elevator contract calls the isLastFloor function twice —first to check if the floor is the last one and then to confirm it,it gets tricked. 
On the first call, isLastFloor says "no". But on the second call, it suddenly says "yes"

-By changing the result between the two calls, we can bypass the check in the Elevator contract, 
successfully setting the last floor as our own.
