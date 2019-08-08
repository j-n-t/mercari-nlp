<img src="https://storage.googleapis.com/kaggle-organizations/1076/thumbnail.jpg%3Fr=260" alt="Mercari Kaggle Competition" height="250" width="250">

# Mercari Price Suggestion Challenge
***

## Challenge description

**Problem:** It can be hard to know how much something’s really worth. Small details can mean big differences in pricing. Product pricing gets even harder at scale, considering just how many products are sold online. Clothing has strong seasonal pricing trends and is heavily influenced by brand names, while electronics have fluctuating prices based on product specs.

Mercari, Japan’s biggest community-powered shopping app, knows this problem deeply. They’d like to offer pricing suggestions to sellers, but this is tough because their sellers are enabled to put just about anything, or any bundle of things, on Mercari's marketplace.

**How to solve it:** In this competition, Mercari’s challenging you to build an algorithm that automatically suggests the right product prices. You’ll be provided user-inputted text descriptions of their products, including details like product category name, brand name, and item condition.

## Evaluation

The evaluation metric for this competition is **Root Mean Squared Logarithmic Error (RMSLE)**.

## Data

### File: train.tsv

This file consists of a list of product listings. This file is tab-delimited and includes the following variables:

* `train_id` - the id of the listing
* `name` - the title of the listing. Note that the data was cleaned in order to remove text that look like prices (e.g. \$20) to avoid leakage. These removed prices are represented as [rm]
* `item_condition_id` - the condition of the items provided by the seller
* `category_name` - category of the listing
* `brand_name` - the product's brand
* `price` - the price that the item was sold for. This is the target variable that we will predict. The unit is USD
* `shipping` - 1 if shipping fee is paid by seller and 0 by buyer
* `item_description` - the full description of the item. Note that the data was cleaned in order to remove text that look like prices (e.g. \$20) to avoid leakage. These removed prices are represented as [rm]

<br>For more information about this challenge, please visit https://www.kaggle.com/c/mercari-price-suggestion-challenge/overview.

## Envisaged solution

Build an algorithm that automatically suggests the right product prices using natural language processing techniques to extract useful information from the text features.