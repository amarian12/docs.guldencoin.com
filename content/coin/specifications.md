---
title: "Specifications"
date: "2014-05-14"
groups: ['coin']
groups_weight: 10
---

## Coin characteristics

 - Algorithm: scrypt PoW KGW
 - TX confirmations: 6
 - Max coins: 1680M
 - Pre-mine: 170M (~10%)
 - Initial difficulty: 0.00244
 - Block reward: 1000NLG
 - Block time: 150 seconds
 - Retarget: 576 blocks (Kimoto's Gravity Well)
 - Block reward halvation: Every 840.000 blocks

## Networks

A main and test network are established. The test network can be used to develop and test applications.

### Main net
 - port: `9231`
 - rpc port: `9232`
 - genesis block: `6c5d71a461b5bff6742bb62e5be53978b8dec5103ce52d1aaab8c6a251582f92`
 - protocol magic: `0xfb, 0xc0, 0xb6, 0xdb`

### Test net
 - port: `9923`
 - genesis block: `f1fe2c7e57300c65ed0e4905ca5f74192a3e1feea209c4fcc2c60df024121a05`
 - protocol magic: `0xfc, 0xc1, 0xb7, 0xdc`
