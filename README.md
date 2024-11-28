# Three-Generations-Seeking-Romance
# A Data Science Approach to Profiling Online Daters According to Age & Generation

This project explores how online dating profiles can be used to predict a user's **age** and the **generation** they belong to (Millennials, Gen X-ers, or Boomers). Using a dataset of nearly 60,000 anonymized entries from the OKCupid platform, we apply supervised machine learning techniques to answer the following questions:

1. **Can your dating profile predict your age?** (Regression - Deep Learning)
2. **Can your dating profile predict the generation you belong to?** (Millennial, Gen X-er, or Boomers) (Classification - Deep Learning)

We will explore various features of user profiles and determine which ones best contribute to accurate predictions. Regression techniques are applied for age prediction, while classification models are used to predict the user's generation.

## Dataset Overview

The dataset contains information about online dating profiles, including personal preferences, demographics, and textual responses from OKCupid users. The columns in the dataset include:

| **Column**           | **Description**                                                                 |
|----------------------|---------------------------------------------------------------------------------|
| **age**              | The age of the person (numerical).                                              |
| **body_type**        | Describes the person's body type (e.g., "a little extra," "thin").              |
| **diet**             | The person's dietary preferences (e.g., "vegetarian," "strictly anything").     |
| **drinks**           | Describes the person's drinking habits (e.g., "never," "socially," "often").    |
| **drugs**            | Describes the person's drug usage (e.g., "never," "sometimes," NaN).            |
| **education**        | The person's educational status (e.g., "working on college," "graduated").     |
| **essay0 to essay9** | Personal essays or responses written by the person.                            |
| **ethnicity**        | The person's ethnic background (e.g., "asian, white," "black").                |
| **height**           | The person's height in centimeters.                                            |
| **income**           | The person's annual income (numerical, with NaN for missing data).             |
| **job**              | The person's occupation (e.g., "transportation," "student").                    |
| **last_online**      | The last time the person was active on the platform (YYYY-MM-DD-HH-MM format). |
| **location**         | The city and state where the person is located (e.g., "San Francisco, CA").    |
| **offspring**        | Information about whether the person has or wants children.                     |
| **orientation**      | The person's sexual orientation (e.g., "straight," "gay," "bisexual").         |
| **pets**             | Whether the person has pets (e.g., "likes dogs," "has cats").                   |
| **religion**         | The person's religious beliefs (e.g., "agnosticism," "Christianity").          |
| **sex**              | The gender of the person (e.g., "m" for male, "f" for female).                 |
| **sign**             | The person's astrological sign (e.g., "gemini," "pisces").                     |
| **smokes**           | Whether the person smokes (e.g., "yes," "no," "sometimes").                    |
| **speaks**           | The languages the person speaks (e.g., "english," "spanish").                  |
| **status**           | The person's relationship status (e.g., "single," "in a relationship").        |

## Objective

The primary goal of this project is to use machine learning techniques to:

1. **Predict the age** of an online dater based on their profile features (Regression model).
2. **Classify the generation** (Millennials, Gen X, Boomers) to which the dater belongs, based on their profile data (Classification model).

### Age Prediction

For age prediction, we utilized **regression models**. Various models were tested and evaluated using the following metrics:

- **R-Squared** (R²)
- **Root Mean Squared Error** (RMSE)
- **Mean Absolute Error** (MAE)

| Model                | R²        | RMSE            | MAE             |
|----------------------|-----------|-----------------|-----------------|
| Gradient Boosting    | 0.835965  | 3.605842        | 2.989767        |
| Ridge                | 0.831213  | 3.657702        | 3.023842        |
| Linear               | 0.831192  | 3.657925        | 3.024430        |
| XGB Regressor        | 0.822859  | 3.747123        | 3.057511        |
| Random Forest        | 0.699469  | 4.880710        | 3.757225        |
| Decision Tree        | 0.680433  | 5.032913        | 3.933287        |
| Extra Trees          | 0.669897  | 5.115205        | 4.029413        |
| Lasso                | 0.596962  | 5.652117        | 4.042815        |
| K-Neighbors          | 0.536311  | 6.062498        | 4.136206        |
| ElasticNet           | 0.331773  | 7.277800        | 5.154753        |

The **Gradient Boosting model** performed the best, with an **R² of 0.836**, explaining **83.6%** of the variation in age. Models like **Ridge** and **Linear regression** also performed well, showing similar R² values.

### Generation Prediction

For predicting the generation (Millennial, Gen X-er, Boomer), we applied **classification models**. The best-performing models were evaluated based on **accuracy**.

| Model                | Accuracy Score |
|----------------------|----------------|
| Gradient Boosting    | 0.672622       |
| Gaussian Naive Bayes | 0.653179       |
| Logistic Regression  | 0.651603       |
| Bernoulli Naive Bayes| 0.646873       |
| Random Forest        | 0.627956       |
| K-Neighbors          | 0.602733       |
| Decision Tree        | 0.535996       |

The **Gradient Boosting Classifier** achieved the highest accuracy score of **0.673**, suggesting it is the best model for classifying users into their respective generations. Other classifiers such as **Gaussian Naive Bayes** and **Logistic Regression** performed slightly worse.

## Conclusion

This project demonstrates how supervised machine learning techniques can be used to predict both **age** and **generation** based on online dating profile features. **Gradient Boosting** models performed the best for both age prediction (regression) and generation classification (classification).
