# Startup-Acquistion-Status-Modelling-on-Crunchbase-Data
*Predicting a Startup’s Acquisition Status The dataset is all about the Startup’s Financial Information and we need to predict the current financial status of the company. The dataset is of Crunchbase - 2013, database, company, investors and all the other details belongs to the company. In this project, we analyzed the company’s status i.e., Operating, Acquired, IPO or Closed.
# EDA
Introduction:

merged_data dataset comprises 196553 rows and 44 columns. --Understanding the Data--
**The dataset is completely based on the company’s information from company’s website database of 2013. **Features: All the columns with the company’s information like name, permalink, category, funding dates, funding rounds, funding amount, city, state, founding dates, last milestone dates and many more. **Target Variable: Status.

--Data Cleaning-- ---We deleted columns with redundancy, granularity and irrelevant information we also deleted instances with missing values for specific columns basically we removed null values for the following columns status, country _code, category_code, founded_at. For the columns with less percentage of null values with used the Imputing method using mean , median and mode.

Data Transformation Here we are fixing irrelevant data types to some columns so we converted columns that include date year datatype.

Then we started filling the null values in closed_at for calculation of the age of company then we created column active_days from subtracting closed_at from founded_at then we removed rows with negative values in active_days and dropped the other two columns

Then we removed outliers using IQR method then we generalized category_code and country_code using One hot encoder to prepare for feature engineering through working on our targeted variable Status and we finalized the data analysis part with deleting duplicates from dataset.

--Model Building---

We started the ML part through applying Logistic Regression Model ,XGBoost Claasifier Model , Quadratic Discriminant Analysis Model and Random Forest Classifier Model . But first we had to prepare the data through the following steps:

-- 1. Splitting the data. We split the data through sklearn ysing test_tain_split function.

-- 2. Separating numerical and Categorical columns

-- 3. Applying one-hot encoding to the whole dataset

-- 4. Scaling the dataset.

Logistic Regression
Logistic Regression helps find how probabilities are changed with actions.
The function is defined as P(y) = 1 / 1+e^-(A+Bx)
Logistic regression involves finding the best fit S-curve where A is the intercept and B is the regression coeffi
Choosing the features
After choosing LDA model based on confusion matrix here where choose the features taking in consideration the deployment phase.
