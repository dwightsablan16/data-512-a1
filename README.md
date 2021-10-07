# DATA 512 Assignment 1: Data Curation
The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2021. All analysis should be performed in a single Jupyter notebook. For this assignment, I combine data about Wikipedia page traffic from two different Wikimedia REST API endpoints into a single dataset, perform some simple data processing steps on the data, and then analyze that data.

## License

The MIT License is a permissive free software license originating at the Massachusetts Institute of Technology (MIT). As a permissive license, it puts only very limited restriction on reuse and has therefore an excellent license compatibility. For more info please see: [MIT license](https://snyk.io/learn/what-is-mit-license/).

## API and Data
In order to measure Wikipedia traffic from 2008-2021, I collect data from two different API endpoints, the Legacy Pagecounts API and the Pageviews API. 

Wikimedia's [Terms of use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)
Wikimedia's [Privacy Policy](https://foundation.wikimedia.org/wiki/Privacy_policy)

- The Legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from December 2007 through July 2016.
- The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month.

Notes: 
- In this analysis, the granularity of data is set to monthly and we collect data for all months where data is available. 
- We're interested in organic (user) traffic, as opposed to traffic by web crawlers or spiders. The Pageview API (but not the Pagecount API) allows you to filter by agent=user. You should do that.
- The main difference among pagecounts and the current pageview data is lack of filtering of self-reported bots, thus automated and human traffic are reported together.

## Data Processing
For this assignment, not much data pre-processing is necessary. 
The steps are as follows:
- Load data from JSON files to pandas dataframes
- Combine mobile-web and mobile-app pageviews
- Create new dataframes for total pageviews and pagecounts
- Drop columns not needed in analysis
- Merge all dataframes into a single dataframe
- Export final dataframe to .csv



## Analysis

[Time-series](https://github.com/dwightsablan16/data-512-a1/blob/main/plot.jpg?raw=true)



