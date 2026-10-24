# **Linear Regression Model for predicting car prices**

We first started with **EDA** (Exploratory Data Analysis), to understand the data we have.

We *removed* null values that represented **less than 5%** of the data.

We encoded the data to be in *float* or *int64* so that the model can understand it easier.

We removed the *Measuring units* from every *feature*  that had a **Measuring unit**.

Then, we made new **dummy columns** to represent *string type data* in **ones** and **zeros**. and removed any *redundant* columns that was not needed, including the **names, torque** because it was hard to decode, and the **first column of every group** of new dummy values derived from a single feature. Because we don't need 2 columns to represent the answer for a question with 2 options, only 1 is enough. 

We plotted a **heatmap** to better understand the relation between our different features.

The **Outliers** above ***Q3 + 1.5 x IQR*** and under ***Q1 - 1.5 x IQR*** was removed from the data, except for the seats, the seats was removed manually only if they contained more than **10 seats**.


SKlearn was used to scale the training data and for training the model.

Every feature was **scalled** with the standard scaler.

The Model had every numeric feature as it's input, and only predicted the selling price.

**Model Scored:**


**R2:**  0.7406053698752109

**RMSE:**  123157.780367556

compared to it's scores on the **training data**: 

**R2:**  0.7232285976027103

**RMSE:**  127411.41100711444

We can conclude that the model didn't overfit or underfit since both scores are similar.

Finally, we ranked every feature on how **significant** it was to the Model using the Models *coef_*.