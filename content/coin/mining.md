---
title: "Mining"
date: "2014-06-21"
groups: ['coin']
groups_weight: 30
---


Mining is the process of adding transaction records to Guldencoin's public ledger of past transactions. This ledger of past transactions is called the block chain as it is a chain of blocks. The block chain serves to confirm transactions to the rest of the network as having taken place. Guldencoin nodes use the block chain to distinguish legitimate Guldencoin transactions from attempts to re-spend coins that have already been spent elsewhere. [from bitcoin wiki/more info](https://en.bitcoin.it/wiki/Mining)

## Mining introduction

Guldencoins are created by a process called "mining". A fixed amount of guldencoins (currently 1000 NLG) is awarded to
the computer that solves a calculation at a specific difficulty. The difficulty is chosen in such way that in average
the calculation is solved in 2,5 minutes. If more or less computers start calculating, the difficulty becomes higher or
lower respectively, to keep in the 2,5 minute average time frame for the calculation to be solved. The calculating power
of the computers in the network is designated in hashes per second.

This "hashes per second" brings us to that calculation that the computers perform. The computers are given a target (at a
specific difficulty) that the computers should reach by performing a hashing calculation. In the case of Guldencoin, this
is the scrypt hashing calculation. The computers will send an input into the hashing calculation, which will return a
result. If this result is better than the target, the input is send to the network and the computer is awarded the
Guldencoins. If the result is not better than the target, a "nounce" (a counter value) is changed in the input and the
hash is run again with a new output to be checked.

The input doesn't contain random data or a nounce only, it contains the transactions send to the network. These transactions
are the payments that shoppers and merchants make when buying and selling goods. By including them into the input data,
their presence will be part of the output. The input that is send to the network and contains the validated transactions,
are called blocks. Other computers in the network can validate if the block is legit by recalculating the input and validate
the output against the difficulty at that time. This way mining stores the transactions in the network.

## Pools

There are several pools mining NLG. Please keep in mind that MH/s evenly spread between pools results in a safer network.

 - [http://nlg.criptoe.com](http://nlg.criptoe.com)
 - [https://nlg.hardcoreminers.com](https://nlg.hardcoreminers.com)
 - [http://gulden.p2p.0x0a.nl:27100](http://gulden.p2p.0x0a.nl:27100)
 - [http://pool.mycryptoco.in](http://pool.mycryptoco.in)
 - [http://dutchpool.org:8000](http://dutchpool.org:8000)
 - [http://dutchpool.org:27100/static](http://dutchpool.org:27100/static)

## Solo

Use the following guldencoind configuration for solo mining:

```
rpcuser=username
rpcpassword=passwordCHANGE-THIS-PASSWORD!!!
rpcport=9232
rpcallowip=127.0.0.1
server=1
daemon=1
listen=1
addnode=seed-000.guldencoin.net
addnode=seed-001.guldencoin.org
addnode=seed-002.guldencoin.nl
addnode=seed-003.guldencoin.net
addnode=seed-004.guldencoin.org
addnode=seed-005.guldencoin.nl
addnode=seed-006.guldencoin.net
addnode=seed-007.guldencoin.org
addnode=seed-008.guldencoin.nl
addnode=seed-009.guldencoin.net
addnode=seed-010.guldencoin.org
addnode=seed-011.guldencoin.nl
addnode=seed-012.guldencoin.net
addnode=seed-013.guldencoin.org
addnode=seed-014.guldencoin.nl
```

### Solo mining with Guldencoin-Qt

* Go to "Help" -> "Debug screen" -> "Console".
* Enter "setgenerate true \<cpu\>" with \<cpu\> the amount of cpu's/cores you want to use for mining.
* Enter "gethashespersec" to see that you are mining.

## GPU mining

You can also mine with the help of your video/GPU card. This results in higher hashrates compared with CPU mining.
Here is a list of cards that have been used in guldencoin mining and their optimal settings:


| *Card*                      | *Hash rate (Kh/s)* | *Settings*                                                 |
|-----------------------------|--------------------|------------------------------------------------------------|
|NVIDIA GeForce GTX 750 1Gb   | 237                | `-i 0 -H 1 -l T4x24`                                       |
|Radeon HD 5970               | 600 - 850          | `-T --compact -I 17 -g 1 -w 128 --thread-concurrency 8000` |
|Radeon HD 7950 4Gb           | 405                | `-I 19 -w 256 --thread-concurrency 22400`                  |


