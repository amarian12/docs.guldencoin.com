---
title: "Explorer"
date: "2014-10-25"
groups: ['services']
groups_weight: 60
---

The Guldencoin team hosts a blockchain explorer dedicated to Guldencoin. The explorer is created and maintained by Geert-Johan,

The explorer is located at [explorer.guldencoin.com](https://explorer.guldencoin.com).

## Beta
Please note that the explorer is currently in Beta.<br/>
<span style="color: red;" >Use information obtained from the explorer at your own risk.</span>

## API
API's are still in development. Some simple api's are available.

### Simple API's
The simple api services return data in plain text format. Coin values are returned in the number of satoshi.

#### Block reward
`/sapi/blockreward` [View](https://explorer.guldencoin.com/sapi/blockreward)

The blockreward service returns the current blockreward following the [formula defined in the original client](https://github.com/nlgcoin/guldencoin/blob/767556cba8ed353fed74d7f3b343ae6815429026/src/main.cpp#L1066-L1078).

#### Total coins
`/sapi/totalcoins` [View](https://explorer.guldencoin.com/sapi/totalcoins)

The totalcoins service returns the current number of coins in circulation. This number is calculated every time a new block is mined. The service combines three sources:

 - Mined coins (excluding premine)
 - Coins distributed among dutch citizens
 - Spent coins from the developer premine

This means that the service returns a very acurate number of coins actually in use.

### JSON API
The JSON API provides information structured using the [JSON](http://json.org/) data format.

No JSON API services have been published yet.
