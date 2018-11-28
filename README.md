# incidentDB_test

The repository used to build the static site is on Github so people can contribute
The CI script provided by the circleci service which is free for one project will build the webpage and host it on Github.

## Why Github

* Provides mechanisms for dispute resolution and contribution of incidents
* Free hosting for open source
* Tools are continually built on Github that you could fork/ adapt to improve the incident DB

## Ops

1. Build the workflow
1. Build the requisite discussion platforms and community incentives (eg. badges)
1. Host bounties for people who report incidents/ help to maintain the page
1. Reserve the analysis/consulting services on the bcss page. This is also a restriction on Github as Github only hosts static pages

## Creating a new incident entry

Make sure that there is no matching incidents in the database. Ideally, also coordinate with the community in [#incidentDB](https://discord.gg/) to prevent conflicting entries. Create a file with a new BID in the [entries](./entries) directory. Use the [template](./entries/template.md) and describe the incident according to the schema as much as possible using publicly available information. 

```
# Title 
Pick a meaningful title.

## Initial Compromise
YYYY-MM-DD, 00:00AM

## Incident Reported 
YYYY-MM-DD, 00:00AM

## Actual Total Loss Estimation in Cryptocurrency
Provide an estimation according to the specific cryptocurrency stolen or lost

## Actual Total Loss Estimation in USD 
Provide an estimation according to prices taken from the time the incident occurred

## Description
Quote from your references the best explanation of what occurred and how it was handled. Remember to notify which source provided the information.
eg. "the DAO hack occurred..." [1]

## Category
Each blockchain incident falls under three categories:
1. OPSEC: incidents compromising an organization or individual’s control of information and access to business-critical assets
2. Smart Contracts: incidents resulting form improperly written smart contracts deployed and executed on a blockchain
3. Consensus Protocol Incentives: incidents arising from malicious exploitation of consensus protocols that create opportunities and benefits for blockchain actors

## Attack Pattern
* If it is a traditional OPSEC incident, please refer to the [CAPEC](https://capec.mitre.org/data/definitions/1000.html) classification by MITRE
* If it is a smart contract incident, please refer to the [SWC-registry](https://smartcontractsecurity.github.io/SWC-registry/)
* If it is a consenss protocol incentive incident please refer to ____

## References
Sources:
Description:
Additional resources:
```
