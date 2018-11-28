# Title
the DAO

## Initial Compromise
2016-06-17, 11:13AM

## Incident Reported
2016-06-17, 13:30PM

## Actual Total Loss Estimation in Cryptocurrency
3544406.91698384ETH

## Actual Total Loss Estimation in USD
75000000

## Description
"An attack has been found and exploited in the DAO, and the attacker is currently in the process of draining the ether contained in the DAO into a child DAO. The attack is a recursive calling vulnerability, where an attacker called the “split” function, and then calls the split function recursively inside of the split, thereby collecting ether many times over in a single transaction."[1]

"On June 5th Christian Reitwiessner discovered an antipattern in solidity which could lead to attacks on smart contracts (later described in a blog post). And then on June 9th, Peter Vessenes wrote a blog about Christian’s discovery. At this point the general Ethereum developer community was aware of this issue. A few days later, Maker DAO (who was also affected) hacked themselves and syphoned their code’s funds into a safe multisig. On June 12th, Eththrowa announced he had found this same antipattern in the DAO, in the reward section of the code. The framework was promptly patched within hours but the deployed codebase could of course not be changed this fast."[2] 

"The DAO (0xbb9bc244d798123fde783fcc1c72d3bb8c189413), its extraBalance (0x807640a13483f8ac783c557fcdf27be11ea4ac7a), all children of the DAO creator (0x4a574510c7014e4ae985403536074abe582adfc8) and the extrabalance of each child are encoded into a list L at block 1880000. The contents of L can be viewed here. At the beginning of block X (X = 1920000, on July 20 or 21 depending on your time zone), all ether throughout all accounts in L will be transferred to contract account C, which is at (0xbf4ed7b27f1d666546e30d74d50d173d20bca754). You can verify the solidity source code of C on etherscan. From this contract, DAO token holders can submit their DAO in order to withdraw ETH at a rate of 1 ETH = 100 DAO. The extrabalance, as well as some additional ether that remains due to complications in the interactions between the re-entrancy exploit and the splitting mechanism, will be withdrawable by the DAO curator to be distributed as appropriate to cover all edge cases."[3]

"We would like to congratulate the Ethereum community on a successfully completed hard fork. Block 1920000 contained the execution of an irregular state change which transferred ~12 million ETH from the “Dark DAO” and “Whitehat DAO” contracts into the WithdrawDAO recovery contract. The fork itself took place smoothly, with roughly 85% of miners mining on the fork.."[4] 

"Let's get into the overview of the attack. The attacker was analyzing DAO.sol, and noticed that the 'splitDAO' function was vulnerable to the recursive send pattern we've described above: this function updates user balances and totals at the end, so if we can get any of the function calls before this happens to call splitDAO again, we get the infinite recursion that can be used to move as many funds as we want.."[5] 

"The Hacker’s Booty Address The DAO hacker withdrew their booty from The DAO on the ETC chain on Sep 5 2016. You can see that the main part of booty still sitting in 0x5e8f0e63e7614c47079a41ad4c37be7def06df5a"" [6]" 

## Category
Smart Contract

## Attack Pattern
SWC-107: Reentrancy

## References
Sources:
* https://blog.ethereum.org/2016/06/19/thinking-smart-contract-security/

* https://dasp.co/timeline.html 

Description:
*[1] https://blog.ethereum.org/2016/06/17/critical-update-re-dao-vulnerability/ 

* [2] https://blog.slock.it/the-history-of-the-dao-and-lessons-learned-d06740f8cfa5 

* [3] https://blog.ethereum.org/2016/07/15/to-fork-or-not-to-fork/ 

* [4] https://blog.ethereum.org/2016/07/20/hard-fork-completed/ 

* [5] http://hackingdistributed.com/2016/06/18/analysis-of-the-dao-exploit/ 

* [6] https://www.bokconsulting.com.au/blog/the-dao-hackers-booty-is-on-the-move/ 

Additional resources:

* Hacker message: https://pastebin.com/CcGUBgDG 

Addresses affected:

* The DAO - https://etherscan.io/address/0xbb9bc244d798123fde783fcc1c72d3bb8c189413 

* DAO creator - https://etherscan.io/address/0x4a574510c7014e4ae985403536074abe582adfc8 

* child DAO - https://etherscan.io/address/0xbf4ed7b27f1d666546e30d74d50d173d20bca754 

* Hacker's ETC - https://gastracker.io/addr/0x5e8f0e63e7614c47079a41ad4c37be7def06df5a

* Example attack transaction:https://www.etherchain.org/tx/d3d4483662185863cde4326ccf5205204adbcda33468587e8153de3fb83a9a37 

* Ether price: https://coinmarketcap.com/currencies/ethereum/#charts 
