# Ethereum Lifetime Lottery
![alt Ethereum Lifetime Lottery](http://www.pineappledeveloper.com/img/ethereum-lifetime-lottery.png)
![alt Ethereum Lifetime Lottery QR-code](http://www.pineappledeveloper.com/img/ethereum-lifetime-lottery-address-qr.png)

The Lifetime Lottery is a simple decentralized peer-to-peer lottery game based on Ether.
Every Ethereum address can join and every new submission fires a reward.

## How does it work?
It's simple: you have to send 0.5 ETH (+ transaction fee) to the smart contract's address (**0xCE9ed0b322A1420Da4b6990e3047796f57471336**)
for registering to the lottery list. After registering, the smart contract chooses
randomly one winning address from the lottery list (including your address)
and sends 0.4 ETH to the winner. The remaining 0.1 ETH are added to the jackpot.
With a chance of 5% the contract hits the jackpot and sends it to the winning address
too.

Once you are registered, you just have to wait for a new submission and for some luck.

## Possible results in more detail
When you send 0.5 ETH to the contract, it adds your address to the lottery list. After that, the 
following results are possible:
+ Your address is the winner and you receive 0.4 ETH. The contract hits the jackpot and you receive
the whole jackpot too.
+ Your address is the winner and you receive 0.4 ETH. The jackpot increases by 0.1 ETH.
+ Any other address from the list is the winner and receives 0.4 ETH. The contract hits the
jackpot and sends it to the winning address too.
+ Any other address from the list is the winner and receives 0.4 ETH. The jackpot increases by 0.1 ETH.

## And why 'Lifetime Lottery'?
I call it 'Lifetime Lottery', because you just have to register once and get the chance
for receiving a reward (or even the jackpot) with every new submission, as long
as the Ethereum Blockchain exists!

## Restrictions
+ For registering, you have to send at least 0.5 ETH to the smart contract's address
(you can send more Ether, but you won't have any benefit from it - it would just increase
the reward, which is immediately redirected).
+ Each address can only be registered once to the lottery list.

## Getters
The Lifetime Lottery serves the following information as Getters:
+ **amountOfRegisters**: it shows, how many addresses are already registered.
+ **currentJackpotInWei**: it shows the current size of the jackpot in wei. Remember, that
one Ether is equal to 10^18 wei.
+ **ourLastWinner**: it shows the address of the latest winner.
+ **ourLastJackpotWinner**: it shows the address of the latest jackpot winner.

## Events
The smart contract logs several events and puts them on the Blockchain.
+ **Received new funds...**: this event is logged, when the contract detects a new submission.
+ **We have a Winner!**: this event is logged, when the contract has picked a winner.
+ **Jackpot is hit!**: this event is logged, when the contract hits the jackpot.
+ **Failed: already joined! Sending back received ether...**: this event is logged, when the contract receives
a funding from an address, which has already been registered to the lottery list.
+ **Failed: not enough Ether sent! Sending back received ether...**: this event is logged, when the contract
receives less than 0.5 ETH.

## Conclusion
Register now, by sending 0.5 ETH to **0xCE9ed0b322A1420Da4b6990e3047796f57471336** for joining the Lifetime Lottery. Good luck!
