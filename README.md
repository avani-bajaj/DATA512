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

## Known issues or special considerations with the data
* Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
* As noted in the Wikimedia APIs section above, there is roughly a year overlap where both APIs provide monthly view count data. During this overlap, data from both APIs is stored and plotted. View counts differ between APIs during this overlap because the newer Pageviews API allows users to filter out non-user initiated page views (crawlers, spiders, bots, etc.), while the older Legacy Pagecounts API does not have this ability.
* The Pageviews API provides monthly view count data for the mobile application and the mobile web site. These values are combined to form the monthly mobile site view count.
* When fetching monthly view count data with both Wikimedia APIs, the end month used as part of the API call is exclusive. The API call will fetch monthly data for all months from the start month up to the end month.

## Data Schema 

Column name	 | Value | Description
------------ | ---------- | ---------------------------------
year | YYYY | Year of Wikipedia traffic from 2008-2017
month | MM | Month of Wikipedia traffic from Jan 2008- Sept 2017
timestamp | MMDDYYYY | Timestamp(Datetime format)to create the time series chart
pagecount_all_views | num_views | Number of pagecounts for mobile and desktop
pagecount_desktop_views | num_views | Number of pagecounts for desktop 
pagecount_mobile_views | num_views | Number of pagecounts for mobile
pageview_all_views | num_views | Number of pageviews for mobile and desktop
pageview_desktop_views | num_views | Number of pageviews for desktop
pageview_mobile_views | num_views | Number of pageviews for mobile
