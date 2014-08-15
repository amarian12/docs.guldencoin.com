---
title: "vanitygen"
date: "2014-07-06"
groups: ['other']
groups_weight: 10
---

Ever seen those 'nice' addresses that start with a recognizable prefix? For instance the addresses used at satoshi dice and nlgcup.com?
You can generate such an address for yourself! With a little tool called 'vanitygen'.

This page describes how to do this. It's assumed that you have some knowledge of the commandline.
This tutorial is for linux.


**Installation**

First of all, clone the [samr7/vanitygen](https://github.com/samr7/vanitygen) repository from github:

`git clone https://github.com/samr7/vanitygen.git`

cd into the directory and build the tool

`> cd vanitygen`

`> make vanitygen`

Now you have built the basic vanity address generator that utilizes the CPU to find an address.

If hou have a good GPU, you might want to use `oclvanitygen`. To compile that run the command:

`> make oclvanitygen`

`oclvanitygen` uses openCL and the GPU to find an address. This is way faster then the normal vanitygen.


**Usage**

Now, lets find a Guldencoin address. You must run vanitygen with the `-X 38` parameter to get an address that works in the Guldencoin network.

`> vanitygen -X 38 Gprefix`

or use `oclvanitygen` instead of `vanitygen` if that applies to you.

Make sure that the address you give to vanitygen starts with a `G`.

Run `vanitygen -h` to get a list of all options.

Once vanitygen found a private key which address matches with the prefix you requested it will print that key.

Copy the key and open your desktop wallet (guldencoin-qt) application. In the menu bar go to `Help > Debug information`. Then open the tab `Console`. In the console type `importprivkey <privKey> MyVanityAddress rescan=false`. Where, ofcourse, <privKey> is replaced with the key you copied from the vanitygen output.

If everything went well, your key has now been added to your wallet. You can now receive on the nice address.
Make sure to test the address before you send any real sums of coins to it. You don't want to lose coins because of a copy-paste mistake..


**Calculation time**

Finding a private key which address matches the prefix you want is hard work. It's actually brute-forcing. Generating new private keys at random and checking if they match. The work is somewhat the same as mining.. The duration of finding one address depends on the length of the prefix you require and the power of your hardware. Vanitygen will display a duration estimage. When it sais it'll take weeks or months to find an addres, don't even try.. It's very likely that it WILL take weeks or months, unless you're really really lucky. The best solution is to shorten the prefix you're trying to find.


**Characterset**

Not all characters are available, this is due to the encoding of the addresses.
https://en.bitcoin.it/wiki/Base58Check_encoding

