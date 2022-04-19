# Trove newspaper totals (historical)

This repository contains past harvests of the number of digitised newspaper articles available through [Trove](https://trove.nla.gov.au/). These harvests were created between 2011 and 2022:

* 12 April 2011
* 4 August 2011
* 12 September 2014
* 29 November 2015
* 14 December 2016
* 28 July 2019
* 10 July 2020
* 27 April 2021
* 21 January 2022

It's possible I might find additional harvests and add them here in the future.

 Since April 2022, datasets have been automatically created every week and saved in [this repository](https://github.com/wragge/trove-newspaper-totals).

## Dataset details

Datasets are saved in the `data` directory as CSV files. There are two types of harvest – one captures the total number of articles per year, while the other breaks the totals down by year and state. The harvest date is embedded in the file title (in `YYYYMMDD` format).

### total_articles_by_year_YYYYMMDD.csv

These datasets are saved as CSV files containing the following columns:

* `year`: year of original publication of newspaper article
* `total`: total number of articles from that year available in Trove

### total_articles_by_year_and_state_YYYYMMDD.csv

These datasets are saved as CSV files containing the following columns:

* `state`: state in which newspaper article was originally published
* `year`: year of original publication of newspaper article
* `total`: total number of articles from that year and state available in Trove

Trove uses the following values for `state`:

* ACT
* International
* National
* New South Wales
* Northern Territory
* Queensland
* South Australia
* Tasmania
* Victoria
* Western Australia

## Method

The method for harvesting this data has changed over time. Harvests from 2011 were screen scraped from the Trove website. Harvests after 2012 make use of the `year` and `state` facets from the Trove API. The data was stored in a variety of locations, such as [this archived page](https://timsherratt.org/shed/trove/graphs/), my Plotly account, and the [Trove Newspapers](https://github.com/GLAM-Workbench/trove-newspapers) GLAM Workbench repository. To create this repository, I've retrieved the harvested data from these locations and converted the datasets to CSV files. Column headings have been normalised, but none of the values have been changed.

For current examples of harvesting this sort of data see [Visualise the total number of newspaper articles in Trove by year and state](https://glam-workbench.net/trove-newspapers/#visualise-the-total-number-of-newspaper-articles-in-trove-by-year-and-state) in the GLAM Workbench.

---

Created by [Tim Sherratt](https://timsherratt.org), April 2022. If you think this is useful, you can become a [GitHub sponsor](https://github.com/sponsors/wragge).