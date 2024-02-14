---
title: "Geographic Harvester"
date: 2024-02-08
lastmod: 2024-02-14
authors: ["Katie Pearson"]
editors: [""]
draft: false
weight: 10
keywords: ["geography","geographic thesaurus","country","continent","state","province","county","municipality"]
---

The Geographic Harvester tool can be used to automatically add geographic units and/or the polygons delineating the borders of geographic units, provided a corresponding geographic unit can be located in the [geoBoundaries API](https://www.geoboundaries.org/) (Runfola et al. 2020). This API includes polygons for many geographic unit ranks.

To use this tool, use the Sitemap to navigate to the Geographic Thesaurus under "Administrative Functions (Super Admins only)" and click "Go to Geographic Harvester" at the top of the page.

The resulting page will show you a list of all countries in the geoBoundaries API and their associated metadata.

* The **In Database** field indicates ....
* The **Has Polygon** field indicates whether that country has a polygon loaded into your geographic thesaurus.
* To view the polygon associated with the country, you can click the **IMG** link in the Preview Image column.

![Geographic Harvester](/symbiota-docs/images/GeoHarvester.PNG)

To import polygons associated with the countries and their lower geographic units, click on the name of the country. The resulting page will show you a list of geographic ranks associated with that country and their associated metadata. For example, the ADM0 rank corresponds to the country, and the ADM1 rank corresponds to the state/province in the U.S.
* The **Database Count** field indicates how many geographic units at that rank are currently in your geographic thesaurus.
* The **Geoboundaries County** field indicates how many geographic untis at that rank are found in the incoming geoBoundaries file.
* To view the raw data associated with the geoBoundaries API call, click the link in the **Full Link** field.
* To view the polygons associated with that geographic rank, click the **IMG** link in the Preview Image field.

![Geographic Harvester Page 2](/symbiota-docs/images/GeoHarvesterRanks.PNG)


The Symbiota Support Hub gratefully acknowledges the work of the geoBoundaries project, which is essential to the functioning of this tool:

**Runfola, D. et al.** (2020) geoBoundaries: A global database of political administrative boundaries. PLoS ONE 15(4): e0231866. [https://doi.org/10.1371/journal.pone.0231866](https://doi.org/10.1371/journal.pone.0231866).
