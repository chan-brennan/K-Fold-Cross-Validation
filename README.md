# K-Fold-Cross-Validation
## 📘 Overview
This RMarkdown report explores the effectiveness of cross-validation methods using the classic iris dataset. The project focuses on predicting petal length based on sepal length through linear and polynomial regression models.

## 🧠 Objective
To investigate whether cross-validation can help determine the better-fitting model (linear vs. quadratic) for predicting petal length from sepal length in iris flowers.

## 🔍 Dataset
Source: Built-in iris dataset in R

Features Used:

- Sepal Length (numeric)

- Petal Length (numeric)

- Goal: Predict Petal.Length using Sepal.Length

## 🧪 Methodology
Exploratory Data Analysis:

- Scatterplot created to visualize the relationship between Sepal.Length and Petal.Length.

Modeling Techniques:

- Linear Regression

- Polynomial Regression (Degree 2)

Validation Techniques:

- Validation Set Approach (50/50 train-test split)

- Leave-One-Out Cross Validation (LOOCV)

- k-Fold Cross Validation (with varying k)

## 📈 Key Steps in the RMarkdown
1. Load and explore the iris dataset.

2. Visualize the data using base R plotting.

3. Split the dataset into training and testing sets.

4. Fit both linear and quadratic regression models.

5. Evaluate performance using multiple cross-validation techniques.

6. Compare models based on Mean Squared Error (MSE).

## 📊 Results Summary
The quadratic model generally produced lower MSEs across cross-validation techniques.

Cross-validation helped confirm that the quadratic fit captured the slight curvature in the data better than a linear model.

## 💾 How to Run
To render the document:

rmarkdown::render("HonorsProject_UPDATED.Rmd")
Make sure the datasets package is available (it's included by default in base R).

## 📌 Dependencies
Base R (datasets, stats)

No additional libraries required
