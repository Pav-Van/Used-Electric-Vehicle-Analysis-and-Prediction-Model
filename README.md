## Installation
 
The Anaconda distribution of Python is needed to run the code, as well as the squarify and lightgbm libraries. The notebook uses python 3.11.3. To download the cars.csv from Github, Git LFS (Large File Storage) is needed.

## Project Motivation

This project analyzes the used electric vehicle market in the United States. As the demand for electric vehicles continues to grow due to enviromental benefits, fuel cost savings, and tax breaks so will the used electric vehicle market. In order to help potential used electrical vehicle buyers, this project will analyze the different trends in the used electric vehicle market and create a price prediction model for electrical vehicles. Using the prediction model and the data analysis in this project, potential buyers can determine if a used electrical vehicle is a good deal or not. The dataset we are using is from Kaggle and was posted by Andrei Novikov. The datatset was created by web scraping the website cars.com and was last updated in April 2023. The initial dataset include all used cars in the United States, but we will only be analyzing the used electric vehicles.

## File Descriptions

* Used_EV_analysis.ipynb - All code is stored in this notebook.
* cars.csv - All used car data is stored in this csv file.
* License.md - License information is stored in this file.

## Results

Our goal was to help aid potential used electric vehicle buyers make a good decision on which used electric vehicles to purchase. After analyzing the data, here are some conclusions:

1. Eventhough Tesla represents more used cars for sale than any other manufacturer, there are other manufacturers like Ford, Nissan, and Chevy that also have a considerable amount of used electric vehicles for sale. 

2. When looking at the price compared with milage, it looks like the prices for Tesla cars decline at a exponential rate the more the milage increases. However, with Nissan, Chevy, and Volkswagen vehicles the price decline is at a linear rate. So Teslas deappreciate in value alot faster than other manfuacturers. 

3. When comparing the seller rating and the price of every manufacturer, Tesla has a lower rating (around 4 out of 5) and a higher price (around $50,000). On the other hand, used electric vehicles made by Chevy and Nissan have a higher rating (around 4.12-4.15 out of 5) and are being sold at a lower price (around $23,000 - $25,000).

My conclusion after these three findings: if you are looking for an electric vehicle do not just default to Teslas because of the name. You may find good deals on highly rated cars from other manufacturers who are working hard to close the gap. Teslas are still great cars, but its worth seeing whats out there.

4. Cars made on or before 2012 have significantly less miles on them than years 2013 and 2014. The buyer should be careful about making purchases on electric vehicles made in 2012 or below even if the car has low milage. The technology back then may be limiting the miles the vehicle will be able to cover over its lifetime.

5. Five predictive models were tested. After cross-validation hyperparameter tuning was performed, the best performing price prediction model was the one that used Light Gradient Boosting. It is fast (.5 secs to train and predict the values) and the error was approximately 2863 which was about the same as the random forest model and better than all the rest. This model could be put into production and be used to help a buyer determine a fair price for a car. The user would enter the different features of a used car they are interested in (Year, Mileage, Model, etc. ). The model would then return a prediction for the price. The error could be added and subtracted from the price to give the limits of a 'Fair Price' range.

You can find the visulizations and insights produced from this report in a read friendly format here: [post](https://medium.com/@Philip_Van/5-insights-on-the-used-electric-vehicle-market-13013229b038)

## Licensing, Authors, Acknowledgements

The credit for the data goes to Andrei Novikov who posted the dataset in Kaggle. You can find the licensing for the data [here](https://creativecommons.org/publicdomain/zero/1.0/). You can find the dataset [here](https://www.kaggle.com/datasets/andreinovikov/used-cars-dataset). Also credit to Udacity for the detailed and helpful lessons given online to help me create this notebook. This code is released under the MIT License.