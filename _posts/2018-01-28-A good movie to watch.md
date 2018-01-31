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

Let us start our EDA by considering the two numerical attributes we have: 'ratings' and 'year'. Before looking at the data one can expect various distribution for these quantities. For example, one can imagine that the rating is distributed uniformly (unlikely), that it peaks at high or low rating, or most likely that it peaks somewhere in the middle. Regarding the year, we already know that there are no reviews after 2013, so the distribution will be truncated.    

What does the data say? First of all the distribution of ratings is not what I was expecting. In particular the distribution looks somewhat Poissonian but there is a high number of movies with 3 stars. It seems like Ebert had a sort of psychological anchor there: not sure about the rating? give it a 3!    

<img src="https://gt987.github.io/assets/images/Ebert/dist.png" alt="">

A more interesting quantity that can be derived from the text is the length of the review. The distribution of length of Ebert's reviews follows very nicely a log-normal distribution. This happens both if you consider the length to be the number of words or the number of sentences in the review. Take a look.

<img src="https://gt987.github.io/assets/images/Ebert/length.png" alt="">

This quite surprising fact is not unique of Ebert's style but is instead a generic human behavior connected somehow with natural language. For those interested you can read more about the occurrence of the log-normal distribution on this [Wikipedia entry](https://en.wikipedia.org/wiki/Log-normal_distribution#Occurrence_and_applications).

## NLP in Python

To be finished...

## GitHub Repo

The code for the analysis is available on my GitHub [repo](https://github.com/gt987/A-good-movie) if you are interested. Enjoy!
