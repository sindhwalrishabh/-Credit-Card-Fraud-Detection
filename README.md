# Credit Card Fraud Detection

This project implements a Machine Learning workflow to detect fraudulent credit card transactions using a Logistic Regression model.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Information](#dataset-information)
- [Methodology](#methodology)
- [Model & Evaluation](#model--evaluation)

---

## Project Overview
Credit card fraud detection is a classic highly-imbalanced classification problem. The goal is to build a model that can identify fraudulent transactions while minimizing false positives to avoid inconveniencing legitimate users.

## Dataset Information
The dataset contains transactions made by credit cards. It is highly unbalanced:
- **Legitimate Transactions (Class 0):** 284,315 transactions
- **Fraudulent Transactions (Class 1):** 492 transactions
- Dataset Link - https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Due to this severe imbalance, standard training would lead to a model biased heavily towards predicting legitimate transactions.

## Methodology
1. **Data Exploration:** Inspected shape, structure, statistical distributions, and checked for missing values (none found).
2. **Under-Sampling:** Created a balanced sub-dataset by randomly sampling 492 legitimate transactions to match the 492 fraudulent transactions, resulting in a new balanced dataset of 984 transactions.
3. **Train-Test Split:** Split the balanced dataset into training (80%) and testing (20%) sets using stratified splitting to preserve class proportions.
4. **Model Training:** Fit a `LogisticRegression` classifier on the training set.

## Model & Evaluation
- **Algorithm:** Logistic Regression
- **Training Accuracy:** ~94.54%
- **Testing Accuracy:** ~94.92%
