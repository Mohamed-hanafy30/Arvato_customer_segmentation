# Arvato_customer_segmentation

A report for Udacity Data Scientist Capstone Project: Create a Customer Segmentation Report for Arvato Financial Services.

This project is a real-life data science task provided by partners at Bertelsmann Arvato Analytics, and it is also served as the Capstone project for Udacity Data Scientist Nano-degree.
In this project, we will analyze demographics data for customers of a mail-order sales company in Germany, comparing it against demographics information for the general population.
Then, we will apply unsupervised learning techniques to perform customer segmentation, identifying the parts of the population that best describe the core customer base of the company. You’ll look at relationships between demographics features, organize the population into clusters, and see how prevalent customers are in each of the segments obtained.

## Project Overview

In this project, you will work with real-life data provided to us by our Bertelsmann partners AZ Direct and Arvato Finance Solution. The data here concerns a company that performs mail-order sales in Germany. Their main question of interest is to identify facets of the population that are most likely to be purchasers of their products for a mailout campaign. Your job as a data scientist will be to use unsupervised learning techniques to organize the general population into clusters, then use those clusters to see which of them comprise the main user base for the company. Prior to applying the machine learning methods, you will also need to assess and clean the data in order to convert the data into a usable form.

## Dependencies 

This project uses Python 3 and is designed to be completed through the Jupyter Notebooks IDE. It is highly recommended that you use the Anaconda distribution to install Python, since the distribution includes all necessary Python libraries as well as Jupyter Notebooks. The following libraries are expected to be used in this project:

This project requires **Python 3.x** and the following Python libraries installed:
- [Numpy](https://numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [Scikit-learn](http://scikit-learn.org/stable/_)
- [Seaborn](https://seaborn.pydata.org/) (for data visualization)
- [matplotlib](http://matplotlib.org/) (for data visualization)

## Why this project?

The unsupervised learning branch of machine learning is key in the organization of large and complex datasets. While unsupervised learning lies in contrast to supervised learning in the fact that unsupervised learning lacks objective output classes or values, it can still be important in converting the data into a form that can be used in a supervised learning task. Dimensionality reduction techniques can help surface the main signals and associations in your data, providing supervised learning techniques a more focused set of features upon which to apply their work. Clustering techniques are useful for understanding how the data points themselves are organized. These clusters might themselves be a useful feature in a directed supervised learning task. This project will give you hands-on experience with a real-life task that makes use of these techniques, focusing on the unsupervised work that goes into understanding a dataset.

In addition, the dataset presented in this project requires a number of assessment and cleaning steps before you can apply your machine learning methods. In workplace contexts, you will frequently need to work with data that is untidy or needs preprocessing before standard algorithms and models can be applied. The ability to perform data wrangling and the ability to make decisions on data that you work with are both valuable skills that you will practice in this project.

## Project Details

Below, you will find an outline of the steps that you will take in this project. It is recommended that you read through all of these instructions before starting on the project so you can build a high-level understanding of the tasks ahead!

### Step 0: The Data

There are a number of files used for this project available in the workspace on the next page. It is strongly recommended that you complete and turn in this project from the workspace. As you will see from the agreement on the next page, if you choose to download a .zip file you will need to REMOVE the files from your computer via the agreement with Arvato Bartlesmann after completing the project, as the data are proprietary. The files available for the project are:

`Udacity_AZDIAS_Subset.csv:` Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
`Udacity_CUSTOMERS_Subset.csv:` Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
`Data_Dictionary.md:` Information file about the features in the provided datasets.
`AZDIAS_Feature_Summary.csv:` Summary of feature attributes for demographic data.

### Step 1: Preprocessing

When you start an analysis, you must first explore and understand the data that you are working with. In this (and the next) step of the project, you’ll be working with the general demographics data. As part of your investigation of dataset properties, you must attend to a few key points:

- How are missing or unknown values encoded in the data? Are there certain features (columns) that should be removed from the analysis because of missing data? Are there certain data points (rows) that should be treated separately from the rest?

- Consider the level of measurement for each feature in the dataset (e.g. categorical, ordinal, numeric). What assumptions must be made in order to use each feature in the final analysis? Are there features that need to be re-encoded before they can be used? Are there additional features that can be dropped at this stage?

**I will create a cleaning procedure that i will apply first to the general demographic data, then later to the customers data.**


### Step 2: Feature Transformation

Now that your data is clean, you will use dimensionality reduction techniques to identify relationships between variables in the dataset, resulting in the creation of a new set of variables that account for those correlations. In this stage of the project, you will attend to the following points:

- The first technique that you should perform on your data is feature scaling. What might happen if we don’t perform feature scaling before applying later techniques you’ll be using?

- Once you’ve scaled your features, you can then apply principal component analysis (PCA) to find the vectors of maximal variability. How much variability in the data does each principal component capture? Can you interpret associations between original features in your dataset based on the weights given on the strongest components? How many components will you keep as part of the dimensionality reduction process?


**I will use the sklearn library to create objects that implement our feature scaling and PCA dimensionality reduction decisions.**

### Step 3: Clustering

- Finally, on your transformed data, you will apply clustering techniques to identify groups in the general demographic data. You will then apply the same clustering model to the customers dataset to see how market segments differ between the general population and the mail-order sales company. You will tackle the following points in this stage:

- Use the k-means method to cluster the demographic data into groups. How should you make a decision on how many clusters to use?
Apply the techniques and models that you fit on the demographic data to the customers data: data cleaning, feature scaling, PCA, and k-means clustering. Compare the distribution of people by cluster for the customer data to that of the general population. Can you say anything about which types of people are likely consumers for the mail-order sales company?

















