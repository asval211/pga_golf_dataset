# Golf Sponsorship Modeling

**Authors:** Elliott Iturbe, Cameron DeArman , Alex Valencia 

## Overview
The goal of this project is to create the best models for owners of a small company in order for them to make a business decision on which golfer they wish to sponsor. Descriptive analyses of data on previous statistics revealed that our models would take in a number of features involving all aspects of the game of golf.

## Business Problem
A Seattle real estate firm would like to create a tool that allows their clients to enter information about their home and receive a prediction for their home's sale price. To help them in this area, we will create a multilinear regression model to help predict the price of a house based off of the properties features.

## Data
We examined data on rounds, gir, average_putts, average_scrambling, average_score, points, top_10, average_sg_putts, average_sg_total, sg:ott, sg:apr, sg:arg, distance_fairway, winners against money.

We examined data on rounds, fairway_percentage, year, avg_distance, gir, average_putts, average_scrambling, average_score, top_10, average_sg_putts, average_sg_total, sg:ott, sg:apr, sg:arg, money against winners.

We also examined data on ounds, gir, average_putts, average_scrambling, average_score, money, top_10, average_sg_putts, average_sg_total, sg:ott, sg:apr, sg:arg, distance_fairway, winners against point_range.


## Methods
Our process started with exploring the data set provided to obtain a stronger understanding of what information we were working with. After some initial analysis of the data replaced a small handful of null values, combining columns in various ways to give us a new featured engeneered column, and changed the datatypes for some of the columns in the data set.

This visualization shows the three most correlated values to Money.

![graph1](./images/3mostcorr.png)

This is a visual illistrates the correlation between the price of the house and the date sold.

![graph2](./images/priceofhomebydate.png)

This visuals x-axis is the predicted values and the y-axis is the true values for the baseline model.

![graph3](./images/baselinescatter.png)

This visuals x-axis is the predicted values and the y-axis is the true values for the final model.

![graph4](./images/Finalmodelscatter.png)


During development we used a basic baseline model for all of our three models which yeilded various scores including accuracy, precision and recall based on which was the appropriate score for the model. As a starting point for all our models to refer back to and make decisions based upon these baseline models. 


## Results
After a good amount of trial and error in the money model, we arrived at our final advanced XGBoost model which yeilded an Accuracy score: for training = .956, validation = .955, and test = .921; as well as a Precision score: for training = .965, validation = .971, and test = .935; followed by a Recall score: for training = .946, validation = .935, and test = .91.

After creating a decent baseline model for winners, we arrived at a final Support Vector Machine model which yeilded an Accuracy score: for training = .894, validation = .895, and test = .895

As for our last model on points, the baseline was not very helpful so we had a lot of work to do and ultimatly landed on a GridSearch using a Decission Tree that gave us an Accuracy score: fot training = .897, validation = .830, and test = .780




# Next Steps
Ideas we had but unfortanatly ran out of time was to take all our models and combine them in a function that you could write a name and year in and get back a Yes or No based of if he made enough money, fell in the correct range of points, and had a chance to be a winner. We also want to expand our understanding of our point range and how we can use our range to predit who would then be in the upperquartile range in future seasons. We also had the idea of being able to put in a single players stats and by our parameters be told by the model if we should sponsor them or not. 

## Conclusions
After many models and tries we created three final model. The models created has given the company. three diffrent measures to evaluate a player, but ultimatly making the decision to sponsor a player comes down to more than the models. A players name and year can be put through the functions provided which give an output on if they predicted either make enough money, fall in the correct points range, as well as if they have a chance to be a winner. However the list of players thatpass these tests are then up for debate amoung the company based on various other attributes suchas character and or social media success. 


## For More Information
Please review our full analysis in [our Jupyter Notebook Money](./report.ipynb), [our Jupyter Notebook Winners](./report.ipynb), [our Jupyter Notebook Points](./report.ipynb) or our [presentation](./microsoftmovieanalysispowerpoint.pdf).

For any additional questions, please contact **Elliott Iturbe at eaiturbe@bsc.edu, Cameron DeArman at cmdearma@bsc.edu, or Alex Valencia at asvalencia1688@gmail.com**

## Repository Structure

```
├── data                                  <- data files used for analyses
├── images                                <- visualizations created
├── notebooks                             <- code written for project with explanation, as well as working ├──notebooks of members
├── microsoftmovieanalysispowerpoint.pdf  <- PDF version of powerpoint
└── README.md                             <- overview of project
```
