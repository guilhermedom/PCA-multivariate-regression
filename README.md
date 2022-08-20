# PCA Multivariate Regression

A quick analysis on multivariate regression using [Principal Component Analysis] (PCA), *[PolynomialFeatures]* and [R2 score] to find a good and simple regression model.

## Problem Overview

Regression analysis is a powerful tool to predict variables when there is historical data to adjust a regression model. However, sometimes the data is not distributed in space in a linear manner, but rather in a polynomial fashion (quadratic, cubic or higher).

Sometimes, the data may be grouped in separate clusters. Take a 2D, dimensionality reduced, [Iris] dataset for instance:

![iris_2d_plot](https://user-images.githubusercontent.com/33037020/185724910-559335df-892b-40af-bd80-9ac823c8af66.png)

A linear regression curve, fitted to Iris' linear features, will achieve a hyperplane that falls in between the two clusters of data:

![iris_3d_plot_regression_hyperplane](https://user-images.githubusercontent.com/33037020/185724917-1fe7327d-0757-48b8-b6df-64f62ec5bae9.png)

## Analysis Introduction

A linear regression model cannot work on a setting with two features scattered in a non-linear manner, since it does not have enough variables to fit a good curve.

To overcome this situation, a good usage of the PCA method can result in a good dimensionality reduction that will generate a dataset with less features, but still being representative of the original data. However, simplifying the data may not be enough to get a simple model that fits well to the data. *PolynomialFeatures* (scikit-learn), on the other hand, is a method that takes linear features and combines them, eventually creating polynomial features.

In this project we use a notebook to analyze multivariate regression models using two popular datasets with distinct challenges involved, [Iris] and [Boston Housing]. We demonstrate how *PolynomialFeatures* and PCA techniques can be combined to help regression models achieve very good performances on datasets with irregular distributions. 

With PCA simplifying our data, and training a regression model using polynomial features, it is possible to find a good fit without needing a complex model.

[//]: #

[R2 score]: <https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html>
[Principal Component Analysis]: <https://en.wikipedia.org/wiki/Principal_component_analysis>
[PolynomialFeatures]: <https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html>
[Iris]: <https://archive.ics.uci.edu/ml/datasets/iris>
[Boston Housing]: <https://www.kaggle.com/code/prasadperera/the-boston-housing-dataset/notebook>
