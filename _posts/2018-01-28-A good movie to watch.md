---
title: "A good movie to watch"
categories:
  - Data Lens
  - NLP
#tags:
#  - nyc
#  - uber
#  - taxi
---

This blog post deals with the incredibly common task of interpreting a language and extracting its sentiment. Humans are obviously very good at this: if I tell you a story or read some article, you understand its meaning; if I tell you a joke or I'm sarcastic, you get it. Computers... not so much...

But for every difficult task there is obviously a big price at the end. Think about how much unexploited data there is in textual resources. Virtually every industry can benefit from Natural Language Processing (NLP): from healthcare to finance, from ads to traveling.

But let us start with small steps. The main goal here is rather simple to state: can Deep Learning classify a bad and good movies based on their reviews? In order to tackle this problem there are various dataset that one can use. IMDB or Rotten Tomatoes are probably the most famous depository of movie reviews, however on this websites the reviews are often written by many different people and therefore both the text and the grading might be inconsistent. For this reason I decided to approach the problem from a different angle and use the reviews written by the famous critic Roger Ebert.

## Data

Ebert has been an incredibly prolific reviewer: nearly 50 years as a critic writer with thousands of reviews under the belt. All his reviews (and many others) are available on [https://www.rogerebert.com](https://www.rogerebert.com) for free. Unfortunately there is no API to access them so I had to gently scrap the website and I made the code available on my [repo](https://github.com/gt987/A-good-movie).

The fields useful for this projects are: year of publication, review, and rating. Overall this fits in a easily manageable dataset of 50 MB.

## EDA

To be finished...

## GitHub Repo

The code for the analysis is available on my GitHub repository if you are interested. Enjoy!
