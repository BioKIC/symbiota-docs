---
title: "Crowdsourcing"
date: 2021-10-07
lastmod: 2024-06-10
draft: false
weight: 40
authors: ["Katie Pearson"]
editors: ["Lindsay Walker"]
keywords: ["crowdsourcing","volunteer","citizen science","community science"]
---

Symbiota has a built-in Crowdsourcing module that can enable any logged-in user to transcribe specimen data from provided images. These specimens must have a [Processing Status](/symbiota-docs/editor/edit/status/) of "Unprocessed" **and** have at least one associated image.

Once a crowdsourcer has transcribed a specimen record and saved the edits, the processing status of the record will be automatically changed to "Pending Review" and the record will be removed from the queue. All edits that have been made to the record will be instantly publicly visible but can be reverted by a collection administrator. The transcribed record is now considered "Pending", and the crowdsourcer will have "pending" points. Once the record is reviewed and approved by a collection administrator (i.e., processing status changed to "Reviewed"), these points will become "approved" points.

Users with administrator permissions can add occurrences to the crowdsourcing queue. Instructions can be found on [this page](https://biokic.github.io/symbiota-docs/coll_manager/crowdsource/edit/).
