AI-Driven Pricing Optimization

Project Overview

This project studies the difference between predicting customer behavior and making an optimal pricing decision.

Instead of trying to directly predict an “optimal price,” the workflow first estimates purchase probability at different price points and then selects the price that maximizes a business objective.

Business Problem

The key question is:

What price should a firm choose when customer purchase probability changes with price and the firm wants to maximize expected profit?

The project demonstrates that pricing is a decision problem, not simply a prediction problem.

Modeling Approach

Models were developed to estimate purchase probability using variables such as:

price;

discount;

product category;

review rating;

customer age;

customer gender;

payment method;

shipping type.

Models included:

Logistic Regression

Gradient Boosting

Logistic Regression provided interpretable purchase probabilities, while Gradient Boosting allowed for nonlinear customer-response patterns.

Price Optimization

After predicting purchase probability, candidate prices were evaluated using expected profit.

For each product category, the workflow:

created a candidate price grid;

predicted purchase probability at each candidate price;

incorporated category-level variable cost;

calculated expected profit;

selected the price with the highest expected profit.

The analysis evaluated categories including:

Books

Clothing

Home & Kitchen

Electronics

Example Optimization Results

The project produced category-level profit-maximizing candidate prices, demonstrating how the optimal decision can vary depending on cost structure and predicted demand.

The broader lesson was that the “right” price depends on the firm's objective. Short-term profit maximization may produce a different pricing decision from a strategy focused on long-term customer value, retention, or acquisition.

Model Evaluation

The project evaluated purchase-probability models using:

ROC-AUC;

log loss;

accuracy;

confusion matrix;

Brier score.

The exercise also noted that unusually strong model performance can be a reason to investigate potential overfitting, low-noise data, or leakage rather than automatically assuming the model will generalize perfectly.

Tools & Technologies

Python

Pandas

NumPy

Scikit-learn

Statsmodels

Gradient Boosting

Logistic Regression

Matplotlib

Optimization / decision modeling

Repository Structure

├── notebook/  
│   └── pricing_optimization.ipynb  
└── README.md

Key Takeaway

Machine learning predicts how customers may respond to price. Optimization then uses those predictions, along with business costs and objectives, to choose the decision that creates the most value.
