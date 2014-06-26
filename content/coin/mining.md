---
title: "Mining"
date: "2014-06-21"
groups: ['coin']
groups_weight: 30
---

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
addnode=seed8.guldencoin.com
addnode=seed9.guldencoin.com
addnode=seed10.guldencoin.com
addnode=seed1.guldencoinseeds.com
addnode=seed2.guldencoinseeds.com
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

| Card              | Hash rate (Kh/s) | Settings                                                 |
|-------------------|------------------|----------------------------------------------------------|
|Radeon HD 5970     | 600 - 850        | -T --compact -I 17 -g 1 -w 128 --thread-concurrency 8000 |
|Radeon HD 7950 4gb | 405              | -T --compact -I 17 -g 1 -w 128 --thread-concurrency 8000 |

