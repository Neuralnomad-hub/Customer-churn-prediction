# Customer-churn-prediction using Artificial Neural Network
# Customer Churn Prediction with Neural Networks: Project Overview

## Project Summary

In this project, I tackled the problem of **customer churn prediction** for a telecom company using artificial neural networks implemented in TensorFlow. Churn, where existing customers leave a service, poses a significant challenge to businesses. By accurately predicting churners, companies can proactively engage at-risk customers and improve retention rates.

## Dataset & Initial Challenges

The analysis was performed on a telecom churn dataset, which included features such as gender, tenure, monthly charges, contract details, and more. One of the initial hurdles involved **handling data quality**:

- The dataset had irrelevant columns like customer ID, which were dropped.
- Some object-type columns (notably total charges) needed conversion to numeric. I encountered missing and error values in these columns and addressed them by removing affected rows to ensure a clean foundation for modeling.
- There were inconsistent entries, like "no internet service" or "no phone service," which I standardized to "no" for simplicity and consistency across feature engineering steps.

## Data Preparation & Feature Engineering

Processing categorical data was essential:

- **Label encoding** was applied to binary columns (e.g., Yes/No, Male/Female), converting them into 1/0 values for the model.
- For categorical columns with more than two categories, I used **one-hot encoding** to create meaningful, model-friendly representations.

A crucial aspect was **feature scaling**—I used MinMaxScaler to scale continuous variables such as tenure and monthly/total charges into a  range. Feature scaling helped the neural network converge efficiently and avoided stability issues.

## Exploratory Data Analysis

Before modeling, visual exploration revealed several trends:

- Customers with **lower tenure** (less loyal) and **higher monthly charges** were more prone to churn.
- I used histograms and color-coded charts to distinguish churners from non-churners, making patterns in the data transparent and actionable.

## Neural Network Modeling

The modeling phase used Keras/TensorFlow:

- The data was split into training and test sets (80/20).
- I designed a **sequential neural network**: input layer, hidden relu-activated layers, and a sigmoid output for binary classification.
- The model was compiled with **binary cross-entropy loss** and the Adam optimizer.
- Starting with modest epochs, I increased training iterations based on initial feedback to achieve optimal accuracy.

## Model Evaluation

Performance was assessed using the test set:

- **Accuracy** reached about 80%, a solid indicator of the model's reliability within this context.
- Predictions from the sigmoid output were thresholded at 0.5 to establish binary outcomes.
- Generated a **confusion matrix** to evaluate true/false positives and negatives, offering insights into the model's predictive strengths and weaknesses.
- Calculated **precision and recall** for a nuanced understanding of how well the model identifies actual churners versus false alarms.

## Skills and Problem-Solving

Throughout the project, I sharpened key data science competencies:

- **Data cleaning**: Special care handling mixed data types and missing entries.
- **Feature engineering**: Applied correct categorical encodings and scaling to support effective model learning.
- **Deep learning framework usage**: Built, tuned, and evaluated neural networks with TensorFlow.
- **Statistical evaluation**: Used advanced metrics like precision, recall, and confusion matrices.

Challenges faced included inconsistent data entries and the risk of data leakage during preprocessing. Systematic cleaning, clear documentation, and stepwise validation addressed these issues methodically. Visualization choices were geared toward maximizing clarity for both technical and non-technical audiences.

## Conclusion

This project demonstrates my ability to approach real-world business problems by:

- **Cleaning and preparing complex datasets**
- **Implementing machine learning models with appropriate evaluation metrics**
- **Translating analytical results into actionable business insights**

The churn prediction model serves as a foundational tool for proactive customer retention strategies and illustrates the value of combining deep learning with rigorous data analysis.
