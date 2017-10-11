---
title: "New Neighbors"
---

I have new neighbors... noisy neighbors! I had noticed that new people were living above my apartment, and I was of course fine with that... until the past weekend, when I woke up at 3 am because of the loud music and pounding on the floor. But hey, I live in NYC, the city that never sleeps. Or at least this is what I thought. (Okay, maybe not the first thing that I thought...)

But is this even true? Are really people in NYC used to noise? Or in other words:
* when do typically people start to complain about noise?
* which are the most noise areas in NYC?

To find an answer to these questions, I have taken a look at the enormous database of calls to the 311.
The database contains...

## Is it too early to call 311?

I pulled from the database 10^5 calls that where categorized as "residential noise". Interestingly enough, most of the time people complain for their neighbors having loud music and dancing (70%), and only sometimes for pounding/banging (25%). Take a look

<img src="https://gt987.github.io/assets/images/calls_dist.png" alt="">

But the most important thing for my good rest is the distribution of calls over time. When is it ok to call 311?

<img src="https://gt987.github.io/assets/images/calls_hist.png" alt="">

As expected most of the calls happen at night and (to my surprise) as early as 9 pm, with a peak at 11 pm.
Just for comparison, my beloved neighbors where still making a mess at 4 am! I guess I won't feel sorrow for shutting down the party the next time...

## Where is the party?

As a fun side-question, one could ask which neighborhood receive most attention. In order to find out, I used a k-neighbors classification with 100 centers and listed the clusters with the highest number of calls. These are the top 3

<img src="https://gt987.github.io/assets/images/noisy.png" alt="">

If you live in NYC, you could try to get there and sneak into a party!
