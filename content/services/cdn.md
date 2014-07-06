---
title: "CDN"
date: "2014-06-19"
groups: ['services']
groups_weight: 60
---


nlgcdn.com is a hosting service for static content aimed at the Guldencoin project and community.
Although the name contains 'cdn', it's not a "real" CDN right now. But when traffic increases, it will become one.
Right now the files are served from a single nginx server.
We chose this solution over existing CDN solutions (maxCDN, Amazon S3, Cloudflare Cache) to avoid vendor lock-in and keep costs low. We can always add one of those solutions in front of nlgcdn.com in a later stage, or preferably: expand nlgcdn.com with self-maintained hosting.

## Directory structure and versioning

The directory structure (paths) follows the following principle:

`/<projectName>/<version>/<contents>`

For instance:

`/guldensign/1.0.0/guldensign.css`

nlgcdn assumes projects to use semantic versioning. If you are unfamiliar with semantic versioning, please read [semver.org](http://semver.org/). It will only take 2-3 minutes to read.

When a project does not use semantic versioning, nlgcdn will try to apply it anyways (best effort).

Although content is only added in a full-version number directory (eg `/project/1.2.3`), there will be symlinks for the mayor and minor versions.

Example symlinks given the content folders: `1.2.1`, `1.2.2`, `1.2.3`, `2.0.1`, `2.1.0`, `2.1.1`.

 - `/project/1.2` -> `/project/1.2.3`
 - `/project/1` -> `/project/1.2`
 - `/project/2.0 -> `/project/2.0.1`
 - `/project/2.1` -> `/project/2.1.1`
 - `/project/2.2` -> does not exist
 - `/project/2` -> `/project/2.1`
 - `/project/3` -> does not exist

## Contents

The contents of this CDN are selected by the Guldencoin team and community. If you think some content is missing, please open an issue at this repository.

### guldensign

[More info about guldensign](/guldensign).

[source on github.com/nlgcoin/guldensign](https://github.com/nlgcoin/guldensign)
