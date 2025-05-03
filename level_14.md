-Gate2: We can call enter() from your contract's constructor. The contract isn't fully deployed during the constructor, so extcodesize will return 0, passing Gate Two.

-Gate3: To pass, we can calculate the correct _gateKey by XOR’ing keccak256(msg.sender) with 0xFFFFFFFFFFFFFFFF. This ensures the XOR condition is met
