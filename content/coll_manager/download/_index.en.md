---
title: "Downloading a Copy of your Database"
date: 2021-11-29
draft: false
weight: 55
authors: ["Katie Pearson", "Lindsay Walker"]
keywords: ["download", "backup"]
---

{{< notice info >}}
  This page describes how to download a copy of your database, including occurrence records, determinations, images (as links only), and any other extensions enabled in your portal (e.g., attribute data).
{{</ notice >}}

It is recommended that curators or collection managers regularly download and archive a copy of their database in case of emergency. Doing so is quick and easy. To download a copy of your data:
1) Navigate to the **_Administration Control Panel_** (_My Profile > Occurrence Management > name of collection_) > **_Download Data Backup File_** (under General Maintenance Tasks)
2) A new window will appear asking you to select the character set (ISO-8859-1 or UTF-8) that will be used in your downloaded dataset. Click the Perform Backup button. The resulting file will be a zipped Darwin Core Archive.

In this folder, your specimen data will be found in a comma-separated (CSV) file named “occurrences,” the specimen identifications in a CSV file called “identifications,” any associated trait data in a file called “measurementOrFact,” and links to related media in a file called “images.” The archive also contains metadata about your collection and about the fields contained in each of the CSV files. For more information about the format and use of Darwin Core Archives, see the following resources:
* [https://github.com/gbif/ipt/wiki/DwCAHowToGuide](https://github.com/gbif/ipt/wiki/DwCAHowToGuide)
* [https://en.wikipedia.org/wiki/Darwin_Core_Archive](https://en.wikipedia.org/wiki/Darwin_Core_Archive)
