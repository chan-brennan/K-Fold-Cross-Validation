# K-Fold Cross Validation – Honors Project

**File**: `HonorsProject_UPDATED.Rmd`  
**Author**: Brennan Chan  
**Date**: March 20, 2025

---

## 📘 Overview

This project uses the popular **iris dataset** (built into R) to explore how well different mathematical models can predict the **length of a flower’s petal** based on the **length of its sepal** (the outer part of the flower).

We try two types of models:
- A **straight-line model** (linear regression), and  
- A **curved model** (polynomial regression, degree 2)

We then test which model works better using a method called **cross-validation**.

---

## 🧠 Objective

To see if cross-validation—a way of testing models—can help us decide whether the straight-line or curved model gives more accurate petal length predictions when we only know the sepal length.

---

## 🔍 Dataset

- **Source**: The built-in `iris` dataset in R  
- **What it contains**: Measurements of flower parts and species names  
- **What we use**:
  - **Sepal Length** (the input)
  - **Petal Length** (the value we want to predict)

**Goal**: Predict petal length based on sepal length.

---

## 🧪 Methodology

### 1. Visual Exploration

We begin by making a scatterplot of sepal length vs. petal length. This helps us see if there's a pattern we can model.

### 2. Models Tested

- **Linear Regression**: Assumes a straight-line relationship between sepal and petal length  
- **Polynomial Regression (Degree 2)**: Allows for a slight curve in the relationship

### 3. Model Testing Techniques

To test how accurate each model is, we use several **cross-validation methods**, which are ways of dividing the data and testing performance:

- **Validation Set Approach**: Split the data in half—train one model, test it on the other half  
- **Leave-One-Out Cross Validation (LOOCV)**: Train on all but one row, test on the remaining row, and repeat for all rows  
- **k-Fold Cross Validation**: Split the data into *k* parts, train on *k–1*, and test on the remaining part—repeat this *k* times

Each technique gives an estimate of prediction error using **Mean Squared Error (MSE)**, which tells us how far off our predictions are from the actual values.

---

## 📈 Key Steps in the RMarkdown

1. Load the dataset and examine the structure  
2. Visualize the relationship between sepal and petal length  
3. Split the data into training and test sets  
4. Train both a linear and a quadratic model  
5. Apply different cross-validation methods to assess accuracy  
6. Compare the models using their average prediction errors (MSE)

---

## 📊 Results Summary

- The **quadratic (curved)** model consistently had a **lower error** than the linear one  
- This suggests the curved model fits the data better, likely because the true relationship is slightly nonlinear  
- **Cross-validation** confirmed that choosing a more complex model (when appropriate) improves prediction

---

## 💾 How to Run

To generate the PDF from the `.Rmd` file, run this in your R console:

```r
rmarkdown::render("HonorsProject_UPDATED.Rmd")
