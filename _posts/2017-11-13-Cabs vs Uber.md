---
title: "Cabs vs Uber"
---

## How is Uber doing?

I pulled from the database 10^5 calls that where categorized as "residential noise". Interestingly enough, most of the time people complain for their neighbors having loud music and dancing (70%), and only sometimes for pounding/banging (25%). Take a look

<img src="https://gt987.github.io/assets/images/CabsVsUber/time.pdf" alt="">

But the most important thing for my good rest is the distribution of calls over time. When is it ok to call 311?

<img src="https://gt987.github.io/assets/images/CabsVsUber/price.pdf" alt="">

As expected most of the calls happen at night and (to my surprise) as early as 9 pm, with a peak around 11 pm.
Just for comparison, my beloved neighbors where still making a mess at 4 am! I guess I won't feel sorrow for shutting down the party the next time!

## Where is the party?

As a fun side-question, one could ask which neighborhood receive most attention. In order to find out, I used a k-means clustering with 100 centers and listed the clusters with the highest number of calls. These are the top 3

<img src="https://gt987.github.io/assets/images/noisy.png" alt="">

If you live in NYC and you want to sneak into a party, I would suggest to try the lower east-side!
