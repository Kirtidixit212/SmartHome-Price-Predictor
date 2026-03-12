# SmartHome-Price-Predictor
SmartHome Price Predictor – Real-Time ML API
Project Overview

SmartHome Price Predictor is a machine learning project that predicts house prices using property features and exposes the trained model through a FastAPI-based real-time API.

The project demonstrates a complete end-to-end machine learning pipeline, including data preprocessing, feature engineering, model training, API deployment, and prediction logging.

This system allows users or applications to send house details and instantly receive predicted property prices through an API.

Problem Statement

Real estate platforms often require quick and reliable property price predictions based on house features such as size, location, and number of rooms. Traditional methods rely heavily on manual estimation.

This project solves the problem by building a machine learning regression model that automatically predicts house prices based on input features and makes the predictions available through an API.

Key Features

End-to-end machine learning pipeline

House price prediction using regression models

FastAPI deployment for real-time predictions

Prediction logging in SQL database

Clean and modular ML workflow

Tech Stack
Programming Language

Python

Machine Learning Libraries

Scikit-learn

Pandas

NumPy

Backend / API

FastAPI

Database

SQL / SQLite

Tools

Jupyter Notebook

Git

GitHub

Machine Learning Workflow
1. Data Preprocessing

Handling missing values

Data cleaning

Feature encoding

2. Feature Engineering

Selecting relevant house attributes

Transforming features for model training

3. Model Training

A regression model is trained using Scikit-learn to learn relationships between house features and price.

Example features:

Square footage

Number of bedrooms

Number of bathrooms

Location attributes

API Development

The trained model is deployed using FastAPI, allowing users to make real-time predictions through HTTP requests.

Example API request:

POST /predict

Input example:

{
  "sqft": 1800,
  "bedrooms": 3,
  "bathrooms": 2,
  "location": "urban"
}

Output example:

{
  "predicted_price": 350000
}
Prediction Logging

Every prediction request is stored in a SQL database including:

Input features

Predicted price

Timestamp

This allows monitoring model performance and collecting data for future improvements.

Project Structure
SmartHome-Price-Predictor
│
├── data
│   └── housing_dataset.csv
│
├── model
│   └── trained_model.pkl
│
├── api
│   └── main.py
│
├── notebooks
│   └── model_training.ipynb
│
├── database
│   └── predictions.db
│
└── README.md
How to Run the Project
Clone the repository
git clone https://github.com/yourusername/smarthome-price-predictor.git
Install dependencies
pip install pandas numpy scikit-learn fastapi uvicorn
Start the API server
uvicorn main:app --reload

The API will run at:

http://127.0.0.1:8000
Future Improvements

Possible improvements include:

Deploying the API on cloud platforms

Adding model monitoring dashboards

Implementing advanced regression models

Building a web interface for predictions

Author

Kirti Dixit
B.Tech Computer Science Engineering
Kurukshetra University

GitHub:
https://github.com/Kirtidixit212

