# Bike-Rental-System

Predict hourly bike rental demand using **Linear Regression** with comprehensive **Exploratory Data Analysis (EDA)**, **feature engineering**, and **Scikit-learn preprocessing pipelines**.

This project demonstrates an end-to-end machine learning workflow, from understanding the data to building, evaluating, and interpreting a regression model.

---

## 📌 Project Overview

Bike-sharing systems generate large amounts of historical usage data. Accurately predicting rental demand helps operators:

* Optimize bike availability
* Reduce shortages and overstocking
* Improve operational planning
* Enhance customer satisfaction

The objective of this project is to predict the **number of bikes rented (`count`)** based on weather conditions, seasonal information, and time-related features.

---

## 📂 Dataset

The dataset contains hourly bike rental records along with environmental and seasonal attributes.

### Features

| Feature    | Description                                      |
| ---------- | ------------------------------------------------ |
| season     | Season of the year                               |
| yr         | Year                                             |
| mnth       | Month                                            |
| hr         | Hour of the day                                  |
| holiday    | Whether the day is a holiday                     |
| weekday    | Day of the week                                  |
| workingday | Whether it is a working day                      |
| weathersit | Weather condition                                |
| temp       | Normalized temperature                           |
| atemp      | Normalized feeling temperature                   |
| hum        | Humidity                                         |
| windspeed  | Wind speed                                       |
| casual     | Casual users *(removed due to data leakage)*     |
| registered | Registered users *(removed due to data leakage)* |
| count      | Total bike rentals (Target Variable)             |

---

## 🎯 Problem Statement

Predict the total number of rented bikes (`count`) using historical weather, seasonal, and temporal information.

---

## 🛠️ Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed detailed data exploration including:

* Missing value analysis
* Data type inspection
* Distribution analysis
* Correlation analysis
* Outlier detection
* Numerical feature visualization
* Categorical feature analysis

---

### 2. Data Preprocessing

Implemented preprocessing using **Scikit-learn Pipelines**.

The preprocessing pipeline includes:

* One-Hot Encoding for categorical variables
* Standard Scaling for numerical features
* Column Transformer for feature management

This ensures reproducibility and prevents data leakage.

---

### 3. Feature Engineering

To improve model performance, several new features were created:

* Month extraction
* Hour extraction
* Month-Hour interaction feature
* Temperature-Humidity interaction feature

Additionally:

* Removed `casual`
* Removed `registered`

These columns directly contribute to the target variable and would cause **data leakage**.

---

### 4. Model Training

Model used:

* **Linear Regression**

The model was trained after preprocessing and feature engineering using a complete machine learning pipeline.

---

### 5. Model Evaluation

The regression model was evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

These metrics provide insights into prediction accuracy and overall model performance.

---

### 6. Model Interpretation

Performed feature importance analysis to understand:

* Which variables contribute most to predictions
* How engineered features affect performance

Interpretability is an important aspect of building trustworthy machine learning models.

---

## 🧰 Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## 📁 Project Structure

```text
Bike-Rental-Prediction/
│
├── data/
│   ├── train.csv
│   └── test.csv
│
├── notebooks/
│   └── Bike_Rental_Model.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🚀 How to Run

Clone the repository:

```bash
git clone https://github.com/ashwinlulla06/Bike-Rental-System.git
```

Navigate to the project directory:

```bash
cd Bike-Rental-System
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Bike_Rental_Model.ipynb
```

Run all cells sequentially.

---

## 📈 Future Improvements

* Experiment with Random Forest Regressor
* Try Gradient Boosting methods (XGBoost, LightGBM, CatBoost)
* Perform Hyperparameter Tuning
* Use Cross Validation
* Build a Streamlit web application
* Deploy the model using FastAPI
* Compare multiple regression algorithms

---

## 📚 Key Learning Outcomes

Through this project I gained hands-on experience with:

* Exploratory Data Analysis
* Data Cleaning
* Feature Engineering
* Preventing Data Leakage
* Scikit-learn Pipelines
* Linear Regression
* Regression Evaluation Metrics
* Model Interpretation
* End-to-End Machine Learning Workflow

---

## 👨‍💻 Author

**Ashwin Lulla**

If you found this project useful, consider giving the repository a ⭐.

