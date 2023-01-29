# AllLife Bank Credit Card Customer Segmentation

## 1. Problem Statement

To identify different segments in the existing customer, based on their spending patterns as well as past interaction with the bank.

## 2. Data Description

Data is of various customers of a bank with their credit limit, the total number of credit cards the customer has, and different channels through which customer has contacted the bank for any queries, different channels include visiting the bank, online and through a call centre.

* Number of observations  - 660
* Number of variables/columns - 7 (all numeric interger values )
* nulls - 0

## 3. Modelling Algorithms

  * K-Means
  * GMM - Gaussian Mixtures Models

*Metrics* -  silhouette_score (), WCSS to select the best number of values

## 4. Results

K-Means is performing good. It was able to group data in three different clusters with clear identification of datapoints to the K center they belong to. GMM is algo giving great results creating almost the same clusters.

As a general note the choice of algorithm here will depend on the context and use case, but for this data set any of them will perform good in production.

![Summary Charts](https://github.com/giomvp/AcademicProjects/blob/7f28836048b0f37089b4cca1813341d48a6d3788/CreditCardCustomer/imgs/summary_plt.jpg)

Complete model selection analysis [here](https://github.com/giomvp/AcademicProjects/blob/7f28836048b0f37089b4cca1813341d48a6d3788/CreditCardCustomer/CreditCardCustomer.ipynb).
