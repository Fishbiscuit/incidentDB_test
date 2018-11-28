# Title
NiceHash payment system compromised

## Initial Compromise
2017-12-06, 1:17PM

## Incident Reported
2017-12-07, 8:19PM

## Actual Total Loss Estimation in Cryptocurrency
4736.43 BTC

## Actual Total Loss Estimation in USD
76833000

## Description
"An attack has been found and exploited in the DAO, and the attacker is currently in the process of draining the ether contained in the DAO into a child DAO. The attack is a recursive calling vulnerability, where an attacker called the “split” function, and then calls the split function recursively inside of the split, thereby collecting ether many times over in a single transaction."[1] 
"(transcribed from youtube livestream from Nicehash)
1. “We became a target and someone really wanted to bring us down.”
2. “We are cooperating with local and international law enforcement”.
3. ~4700 BTC stolen on early morning 12-06-2017
4.Can’t discuss everything due to investigation.
5. Hacker(s) were able to infiltrate our internal systems through a compromised company computer.
6. Unknown how company computer was compromised.
7. VPN had visibility into abusive behavior, IP address was outside of European Union.
8. “Made a crucial VPN login using an engineer’s credentials”
9. After VPN login, learned and simulated the workings of our payment system.
10. Managed to steal funds from accounts (indicates that the active attack timeline was only a couple hours)" [1]
"NiceHash, a cryptocurrency mining marketplace, confirmed that its security has been breached and “the contents of the NiceHash Bitcoin wallet have been stolen.” Its users said in online forums that their balances are zero and that more than $60 million was moved to a Bitcoin wallet on December 6." [2]
"Official press release statement by NiceHash: 
Unfortunately, there has been a security breach involving NiceHash website. We are currently investigating the nature of the incident and, as a result, we are stopping all operations for the next 24 hours. Importantly, our payment system was compromised and the contents of the NiceHash Bitcoin wallet have been stolen. We are working to verify the precise number of BTC taken...Here is the hacker BTC address https://bitinfocharts.com/bitcoin/address/1EnJHhq8Jq8vDuZA5ahVh6H4t6jh1mB4rq[5]" [3]
"NiceHash executive Andrej P. Škraba told Reuters that his firm was the victim of “a highly professional” heist that yielded about 4,700 bitcoin, worth around $64 million." [4]

## Category
OPSEC

## Attack Pattern

CAPEC-255: Subvert Access Control 
CAPEC-560: Use of Known Domain Credentials 
CAPEC-555: Remote Services with Stolen Credentials 


## References
Sources:

* https://magoo.github.io/Blockchain-Graveyard/ 
* [1] https://www.youtube.com/watch?v=h4AqlLqUhnw 

Description:

* [2] https://www.wikitribune.com/story/2017/12/06/tech/cryptocurrency-site-nicehash-confirms-hack/26595/ 

* [3] https://www.reddit.com/r/NiceHash/comments/7i0s6o/official_press_release_statement_by_nicehash/ 
* [4] https://www.reuters.com/article/us-cyber-nicehash/hackers-steal-64-million-from-cryptocurrency-firm-nicehash-idUSKBN1E10AQ 

Additional resources: 

* Addresses affected: [5] https://bitinfocharts.com/bitcoin/address/1EnJHhq8Jq8vDuZA5ahVh6H4t6jh1mB4rq 
