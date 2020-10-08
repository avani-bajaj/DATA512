# DATA512
Repository for UW course DATA 512

## Assignment 1 : Data Curation 
Data curation is the management of data throughout its lifecycle, from creation and initial storage to the time when it is archived or becomes obsolete and is deleted.

Goal : 
The goal of this assignment is to acquire, process, and analyze a dataset of monthly traffic on English Wikipedia from December 2007 to August 2020, inclusively. The steps taken are meant to be fully reproducible.

In this assignment, all these 3 stages to create a completely reproducible project. Following are the steps taken:

### 1. Data Acquisition

* Set API endpoints for the Pagecounts API and the Pageviews API
* Set Parameters to make the 'Pagecounts' and 'Pageviews' API calls
* Make Pagecount and Pageview API calls to get mobile, desktop and both Wikipedia traffic data. The output is json file which is saved on disk.

### 2. Data Processing

* Load data from json response into the respective list for time, mobile, desktop and all site views/counts.
* Write the lists in a single dataframe for pagecount and pageviews
* Merge the pagecount and pageviews dataframe into a single dataframe
* Write the dataframe in a csv file and save it to disk

### 3. Data Analysis

*Create a plot to visualize Wikipedia traffic data Visualize Wikipedia traffic with 3 metrics: mobile traffic(for counts and views), desktop traffic(for counts and views) and all traffic (mobile + desktop)
* Save the visualization as an image file (saved as png file)

### Final visualization 
![Page Views on English Wikimedia](https://github.com/avani-bajaj/DATA512/blob/main/data512-a1/PlotPageviewsWiki.png)

## License of the source data 
[MIT License](https://opensource.org/licenses/MIT)
## Wikimedia terms of use 
We can find the Wikimedia Terms of use [here](https://wikimediafoundation.org/wiki/Terms_of_Use/en)

## Relevant API documentation
* [Documentation on Pagecounts](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)
* [Documentation on Pageviews](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)

## Source data
Json files from api calls:

* pagecounts_desktop-site_200801-202008
* pagecounts_mobile-site_200801-202008
* pageviews_all-sites_201507-202008
* pageviews_mobile-app_201507-202008
* pageviews_mobile-web_201507-202008


[Lets go to Quora](https://www.quora.com)

