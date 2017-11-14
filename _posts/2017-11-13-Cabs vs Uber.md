---
title: "Cabs vs Uber"
---

Since the introduction of the iPhone, our lives and habits have changed dramatically, and one of these big changes involves the way we travel around cities. For example, 10 years ago we used to raise our arm to call a cab, nowadays we most likely go for our phones, and probably in some years we'll summon a driverless car using our watch. Moreover, all these changes are also affecting companies that haven't been able to evolve (think about Nokia) and entire compartments of the economy (sorry drivers...).

In this post I will take a look at the traditional cab companies operating in NYC and see how they are doing in the era of Uber. Are they doing well or just dying slowly? To answer these kind of questions I used the data of the The New York City Taxi & Limousine Commission (TLC) which has made publicly available a [gigantic database](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml) of all the rides of the Yellow, Green and FHV (For Hire Vehicle) companies in NYC from 2009 to present.

This database can obviously answer a bunch of interesting questions and should be exploited much more than what I will be showing here. To mention some possible direction:
* When and Where should vehicles stay to maximize total income?
* How bad is rush hour?
* Is it better to take a cab or a city bike or the metro?
* Are you tipping too few?
* ...

## Data

The TLC provides a monthly dataset for each of the three categories of vehicles operating in NYC (Yellow, Green and FHV). The average dataset contains around 10^8 rides and weights around 1 GB. In total it contains roughly a billion rides (yes a billion!) for a total of 250 GB. In fact it is so big that it does not fit on my laptop.

Fortunately a large part of it can be already found on [BigQuery](https://cloud.google.com/bigquery/public-data/nyc-tlc-trips), and can be assessed via simple SQL queries. The 2017 data is not there, so I downloaded them directly from TLC. For an explanation on how to retrieve the information you'll see below, take a look at [the GitHub repository](https://github.com/gt987/Cabs-vs-Uber).

The FHV data provided by TLC is not as exhaustive as the Yellow and Green data as it often contains only the license ID and the pickup time. It is however sufficient to individuate the amount of trips made by Uber cars. Notice also there is an error in how BigQuery retrieves the FHV data in June 2015, which I've fixed by looking at the original TLC data.  

## Bye Bye cabs...

The main point of this post is summarized in the next figure, where I plot the amount of trips made by each company per month. I think there are three main take-home messages:
1. Uber is overtaking the Yellow Cab company (which lost 30%  of its customers in the last 3 years).
2. Uber has changed our habits as people are more likely to take a ride.
3. At this pace, the traditional companies will be closing business in 3 years.

<img src="https://gt987.github.io/assets/images/CabsVsUber/time.png" alt="">

One may think that with the falling number of rides and additional competition the prices of the Yellow and Green cabs would fall. However this does not seem to be the case. In fact looking at the average trip cost in the next plot, it seems that prices have been pretty constant in the past years. (Unfortunately no data from Uber.)

<img src="https://gt987.github.io/assets/images/CabsVsUber/price.png" alt="">

## GitHub Repo

The data for these plots are available on the GitHub repository if you are interested in doing your own analysis.
