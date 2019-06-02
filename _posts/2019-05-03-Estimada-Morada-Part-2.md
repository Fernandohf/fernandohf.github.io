---
layout: post
title: Real Estate Model, Part 2 - Getting the Data
---

In this post we will focus on how to acquire the data needed to train our model. We will discuss everything that should be considered such as the possible problems and inconsistencies present in scraped data sources.

## Summary

List of posts:

1. [Real Estate Model, Part 1 - Defining the Problem]()
2. [Real Estate Model, Part 2 - Getting the Data]()

## Expected Data Format - Tabular

![_config.yml]({{ site.baseurl }}/images/02/features.png "Source: <https://undraw.co>")

In the last post, we formulated and defined our problem: **Predict Real Estate Values**. Now that our problem is clearly defined, we can start working on how to model it. It is reasonable to think that the price of houses/apartments are dependent of the their features such as number of room, area, locations, etc. Or course, there are some intrinsic uncertainties related to this problem. E.g. some characteristics are not easily definable: local market, close constructions, flooding area, haunted(😨), etc. As said in the previous post, remember to always maintain clear all your assumption along the process.

> House prices are dependent of the house features such as number of room, area, locations, etc.

Therefore, we will use the properties described in the house listing as the inputs to the house price.

## Data Sources

![_config.yml]({{ site.baseurl }}/images/02/search.png "Source: <https://undraw.co>")

There is an important question that need to be answered: Where and how do we get our data? The World Wide Web is a great source for the database that you are looking for. Multiple sites ([Kaggle](https://kaggle.com/), [UCI](https://archive.ics.uci.edu/ml/index.php, [Google Datasets](https://ai.google/tools/datasets/), ...) provide well-known datasets for famous problems, and, multiple times, they are a great source to solve your problem. In general, these databases are in a tabular format and fairly clean. However, often these datasets are not specific enough for our problem. For example, it is easy to find a dataset with house/apartments description and pricing, but from a completely different region of the world. Therefore, we should look for data that reflects our problem.

### Web Scraping with BeautifulSoup

Web scraping is a technique to extract data publicly available on the web. Multiple websites have listings of real estate descriptions and pricing, making them a perfect source of our dataset. This process is considerably more time consuming and demanding, but it results in a database that faithfully describes our problem. We will be using [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) to extract our data from static listing websites.

# Copy Beautiful CODE


## References

