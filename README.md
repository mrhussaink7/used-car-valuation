# Choosing The Right Used Car with Price Modeling

![image](https://github.com/mrhussaink7/used-car-valuation/blob/main/images/dataset_cover.png)

*Image Found on DepositPhotos.com*

## Overview

We've developed a used car price prediction model using data from Craigslist car listings. This model helps consumers by estimating the fair market value of a car, indicating if a listing is a good deal, bad deal, or fair deal based on the difference between the predicted and actual prices.

As the data scientist on this project, my goal was to analyze the car listings and provide insights that assist consumers in making informed buying decisions. By leveraging various car features such as make, model, year, and mileage, we offer a comprehensive guide for evaluating car prices.

Analysis by Kawsar Hussain

## Challenge

Our goal is to provide actionable recommendations to consumers that will directly impact their car buying decisions. Using data-driven insights from the Craigslist Used Car Price Prediction project, we aim to offer three key recommendations that will optimize purchase strategies and ensure consumers get the best value for their money. These recommendations are grounded in evidence and are designed to deliver tangible benefits to car buyers.

## Datasets

In the folder `data`, we have datasets from:

- [Kaggle Data Scraped From Craigslist](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)

## Solution

By building a model that predicts car price, we can further evaluate if the car is within market trends to show the consumer whether the purchase would be a worthwhile and if they are getting a good deal or not. These recommendations are grounded in evidence and are designed to help consumers identify the best deals, avoid overpaying, and make informed choices, ultimately benefiting their car buying experience.

## Results

### 1. Focus on Key Features: Year, Odometer, and Condition

`Insight:` Year and odometer readings are the most significant factors influencing car prices, as newer cars with lower mileage typically have higher values. Whereas condition has low weight on price.

`Recommendation:` Prioritize these factors when evaluating used cars, as they are reliable indicators of market value.

![image](https://github.com/mrhussaink7/used-car-valuation/blob/main/images/solution_1.png)

### 2. Be Cautious of Reported Condition

`Insight:` The reported condition often does not significantly impact price, likely due to inconsistent reporting. "Like new," "excellent," and "good" cars are often similarly priced, while "fair" cars can sometimes be cheaper than "salvage."

`Recommendation:` Don't rely solely on the listed condition. Thoroughly inspect the car or hire a professional to verify its true state.

![image](https://github.com/mrhussaink7/used-car-valuation/blob/main/images/solution_2.png)

### 3. Utilize the Price Error Range for Negotiations

`Insight:` The model's error range, around 18% or $2207, can indicate if a car is fairly priced. The model tends to underestimate higher-priced cars and overestimate lower-priced ones.

`Recommendation:` Use this error range in negotiations. If a car is listed above the predicted price, it may be overpriced. If below, it might be a good deal, but verify for hidden issues.

![image](https://github.com/mrhussaink7/used-car-valuation/blob/main/images/solution_3.png)

## Practical Use-Case
Our model essentially takes used vehicle details and outputs a predicted price and a determination of whether it's a good deal, bad deal, or fair deal, based on the threshold of whether it exceeds, within, or below the price error range outputted by the model.

![image](https://github.com/mrhussaink7/used-car-valuation/blob/gating/images/test_practical_use_case.png)

## Conclusion

- #### Key Features Matter: Year and odometer readings are crucial for determining used car prices and should be prioritized when evaluating a vehicle.
- #### Reported Condition Is Unreliable: The listed condition may not accurately reflect a car's true state, making thorough inspections essential.
- #### Use Price Predictions Wisely: The model's error range can guide negotiations, helping identify overpriced or potentially good deals.

## Next Steps

- #### Refine the Model with Carfax Data: Integrate Carfax data to gain a more accurate understanding of vehicle conditions and improve model predictions.
- #### Gather Customer Reviews: Collect customer reviews to better understand different car models and enhance the model's insights.
- #### Deploy Basic Model on Website: Implement the basic model on our car section, allowing customers to see if a car is a good deal, bad deal, or fair deal as they navigate different listings.

## Repository Structure
```
├── code
│   ├── data_preparation.ipynb
│   ├── exploratory_data_analysis.ipynb
│   ├── model_development.ipynb
│   ├── model_evaluation.ipynb
├── data
│   ├── clean_vehicles.csv.zip
│   ├── subset_vehicles.csv
├── images
│   ├── dataset_cover.jpg
│   ├── solution_1.png
│   ├── solution_2.png
│   ├── solution_3.png
│   ├── test_practical_use_case.png
├── LICENSE
├── README.md
├── craigslist_used_car_deals_presentation.pdf
```
