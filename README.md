# Capstone Project: Bertelsmann - Arvato Customer Segmentation & Modeling

## Table of contents
1. [Project Motivation](#motivation)
2. [Installation](#installation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## 1. Project Motivation <a name="motivation"></a>
This project is the Capstone of the Data Scientist Nanodegree Program with Udacity. 

It is made in collaboration with Bertelsmann-Arvato. The goal of our project is to foresee, which part of the population is most likely to convert to a customer, after being targeted with a mailing campaign. To do so, we will follow two mail steps:

  - Unsupervised leaning techniques to segment the general German population and compare it to our customers dataset.
  - Supervised learning model to predict reaction probability on marketing campaign.

Read the complete report on this project by clicking on the following link: https://medium.com/@maria.milman.moschenko/capstone-project-with-udacity-bertelsmann-arvato-customer-data-segmentation-566ca2d3f7ec

## 2. Installation <a name="installation"></a>

The project was implemented using Python. The main libraries used include:

- `numpy`, `pandas` – Data manipulation
- `matplotlib`, `seaborn` – Data visualization
- `scikit-learn` – Preprocessing, modeling, and evaluation
- `xgboost` – Advanced gradient boosting model
- `imblearn` – Handling imbalanced datasets
  
## 3. Files Descriptions <a name="File Descriptions"></a>
- ‘Udacity_AZDIAS_052018.csv’: Demographics data for the general population of Germany; 891 211 persons (rows) x 366 features (columns).
- ‘Udacity_CUSTOMERS_052018.csv’: Demographics data for customers of a mail-order company; 191 652 persons (rows) x 369 features (columns).
- ‘Udacity_MAILOUT_052018_TRAIN.csv’: Demographics data for individuals who were targets of a marketing campaign; 42 982 persons (rows) x 367 (columns).
- ‘Udacity_MAILOUT_052018_TEST.csv’: Demographics data for individuals who were targets of a marketing campaign; 42 833 persons (rows) x 366 (columns).
- For more information about the columns depicted in the files, you can refer to two Excel spreadsheets provided in the workspace. DIAS Information Levels — Attributes 2017.xlsx is a top-level list of attributes and descriptions, organized by informational category. DIAS Attributes — Values 2017.xlsx is a detailed mapping of data values for each feature in alphabetical order.

Based on the T&C agreed with Bertelsmann, the four datasets are not available on GitHub to use or see.

## 4. Results <a name="results"></a>

In this project, we successfully segmented the customer base and built a predictive model to identify likely responders to a marketing campaign.

1) In the unsupervised learning phase, we:

- Cleaned and preprocessed the demographic data from the German population and customers
- Reduced the dimentionality using PCA capturing the most important components.
- Performed clustering with K-Means to identify distinct population segments.
- Compared the distribution of clusters between the general population and customers to detect segments with higher customer representation. This analysis gave us insights into which types of individuals are more likely to become customers.

2) In the supervised learning phase, we:

- Preprocessed the mailout_train dataset, handling missing values and encoding categorical variables.
- Trained 5 different models and evaluating them using ROC AUC as the primary metric to account for class imbalance.
- Tuned hyperparameters to optimize performance, with the best model achieving a ROC AUC score of 0.773.
- Applied the final model to the mailout_test dataset to generate probability scores for each individual’s likelihood to respond positively to a mailing campaign.
- These steps have allowed us to both understand the characteristics of the existing customer base and build a data-driven model to target future marketing efforts more effectively.

## 5. Licensing, Authors, and Acknowledgements <a name="licensing"></a>
Thank you Bertelsmann — Arvato for providing these datasets.
I also want to thank Udacity for all the training materials, previous project experience and the mentors (especially Rajat) on the Knowledge exchange platform. This project was a personal challenge, which I enjoyed and had the chance to learn very much during the process.
