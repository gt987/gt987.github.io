---
title: "New Neighbors"
categories:
  - Data Lens
#  - Services
#tags:
#  - nyc
#  - 311
---

A couple of weeks ago I noticed that some new tenants had moved in the apartment above mine and I was of course fine with that... until they woke me up at 3 am. Loud music, dancing, jumping and all of that...

But hey, I live in NYC, the city that never sleeps. Or at least this is what I thought. (Okay, maybe not the first thing that I thought...)

But is this even true? Are really people in NYC used to parties? Or in other words:
* when do typically people start to complain about noise/music?
* which are the most noisy areas in NYC?

To find an answer to these questions, I have taken a look at the enormous [database](https://opendata.cityofnewyork.us) of calls to the 311.
The database contains information about the service requests made in NYC since 2010 (roughly 16 millions). I needed a very limited amount of information for the following exploration, but if you want to explore more, you can find the my notebook [here](https://github.com/gt987/311-Service-Request).

## Is it too early to call 311?

I pulled from the database 10^5 calls that where categorized as "residential noise". Interestingly enough, most of the time people complain for their neighbors having loud music and dancing (70%), and only sometimes for pounding/banging (25%). Take a look

<img src="https://gt987.github.io/assets/images/New Neighbors/calls_dist.png" alt="">

But the most important thing for my good rest is the distribution of calls over time. When is it ok to call 311?

<img src="https://gt987.github.io/assets/images/New Neighbors/calls_hist.png" alt="">

As expected most of the calls happen at night and (to my surprise) as early as 9 pm, with a peak around 11 pm.
Just for comparison, my beloved neighbors where still making a mess at 4 am! I guess I won't feel sorrow for shutting down the party the next time!

## Where is the party?

As a fun side-question, one could ask which neighborhood receive most attention. In order to find out, I used a k-means clustering with 100 centers and listed the clusters with the highest number of calls. These are the top 3

<img src="https://gt987.github.io/assets/images/New Neighbors/noisy.png" alt="">

If you live in NYC and you want to sneak into a party, I would suggest to try the lower east-side!
