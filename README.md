# Predicting Football Team Positions in the Premier League Table
![Python](https://img.shields.io/badge/python-v3.6+-blue.svg)

## Overview

This project focuses on utilizing machine learning techniques to predict the positions of football teams in the Premier League table based on various statistical features. The dataset used contains information on matches played, including home and away teams, goals scored by each team, chances created, saves made, and shots blocked. By analyzing these factors, the aim is to develop a model that can accurately predict the final positions of the teams in the league table.

## Dataset

The dataset used in this project is sourced from the Premier League and contains the following columns:

    Home Team: The name of the home team.
    Away Team: The name of the away team.
    Goals Home: The number of goals scored by the home team.
    Away Goals: The number of goals scored by the away team.
    Home Chances: Chances created by the home team.
    Away Chances: Chances created by the away team.
    Home Saves: Saves made by the home team.
    Away Saves: Saves made by the away team.
    Home Blocked: Shots blocked by the home team.
    Away Blocked: Shots blocked by the away team.

## Data Preprocessing

Before applying machine learning algorithms, some preprocessing steps are performed:

- Basic statistics are generated to gain insights into the dataset.
- Null values are checked to ensure data integrity.
- Correlation analysis is conducted to identify relationships between different features.

## Exploratory Data Analysis (EDA)

EDA is performed to visualize and understand the distribution and relationships between variables:

1. Scatter plots are used to visualize the relationship between chances created and goals scored.
2. Histograms are used to visualize the game results.

<p align="center"><img width=45% src="https://github.com/p4trykk/Premier-League---prediction-ML-model/blob/main/images/wykres1.png">
<img width=45% src="https://github.com/p4trykk/Premier-League---prediction-ML-model/blob/main/images/wykres3.png"></p>

3. Histograms are plotted to analyze the distribution of goals scored by home and away teams.

<p align="center"><img width=65% src="https://github.com/p4trykk/Premier-League---prediction-ML-model/blob/main/images/wykres2.png"></p>

## Model Development

Machine learning models are developed to predict team positions based on historical data. The following steps are involved:

1. Data from previous seasons is collected and processed.
2. Features such as goals scored, goals conceded, and positions are extracted.
3. The dataset is split into training and testing sets.
4. Ridge regression is employed as the predictive model due to its ability to handle multicollinearity (show below).

<p align="center"><img width=55% src="https://github.com/p4trykk/Premier-League---prediction-ML-model/blob/main/images/wykres4.png"></p>

## Results and Evaluation

After training the model, it is evaluated using the testing set. Performance metrics such as mean squared error (MSE) and R-squared score are calculated to assess the model's accuracy in predicting team positions.

#### Output
```text
------------ Model results ------------
Mean Squared Error: 0.00466376712179851
R^2 Score: -1.0794038604013099
```
- Mean Squared Error (MSE): The MSE measures the average of the squares of the differences between predicted and actual values. A lower MSE value suggests that the model fits the data well, but it's not the sole indicator of effectiveness.
- Coefficient of Determination (R^2 Score): The R^2 Score measures how well the model fits the data. A value close to 1 indicates a perfect fit, while a value close to 0 means the model does not explain any variability in the data. A negative value, as in this case, indicates that the model performs significantly worse than a model that simply predicts the mean value for all observations.


## Predictions

Finally, the trained model is applied to predict the positions of football teams in the upcoming season based on their goals scored and conceded. The predicted positions provide insights into the potential performance of each team in the league.

```text
------------ Model predictions ------------
Arsenal: 1.8463082350699196
Wolverhampton Wanderers: 16.61794166524439
Aston Villa: 10.82589203318864
Brighton and Hove Albion: 6.516108524489196
Brentford: 9.178360791603218
Manchester City: 1.0
Chelsea: 13.975994369855398
Newcastle United: 5.649525759518525
Crystal Palace: 13.686074076847227
Nottingham Forest: 15.874425018025853
Everton: 15.821455387985381
Bournemouth: 16.380991002276694
Leeds United: 14.424823552984993
Tottenham Hotspur: 7.890846330737627
Leicester City: 12.814724140795786
West Ham United: 13.757759621585807
Manchester United: 8.907156413293155
Fulham: 10.517255825482362
Southampton: 16.797155527090844
Liverpool: 5.26761495004674
```

## Conclusion

In conclusion, this project demonstrates the application of machine learning techniques in predicting football team positions in the Premier League table. By analyzing historical data and leveraging predictive models, it becomes possible to make informed decisions and predictions regarding team performances in future seasons.
