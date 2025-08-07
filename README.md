# 🛠️ Titanic Survival Prediction - Logistic Regression Project

This project aims to predict the survival of passengers aboard the Titanic using a **Logistic Regression** model. It involves **structured data preprocessing**, **exploratory data analysis**, **feature engineering**, and **model evaluation** – all implemented in Python with libraries such as **Pandas**, **Seaborn**, **Matplotlib**, and **Scikit-learn**.

## 📌 Project Overview

The Titanic dataset is a classic machine learning dataset used for binary classification problems. In this project, we:
- Cleaned and preprocessed the dataset
- Conducted exploratory data analysis (EDA) to identify important features
- Converted categorical variables into numerical format
- Built a logistic regression model to predict survival
- Evaluated the model using accuracy and other performance metrics

## 📋 Step-by-Step Workflow

### 1️⃣ Data Import & Inspection
- Loaded the dataset using **Pandas**
- Explored the dataset using `.head()`, `.info()`, and `.describe()` to understand structure, null values, and data types

### 2️⃣ Data Cleaning
- **Dropped** the `Cabin` column due to excessive missing values
- **Filled** missing values in the `Age` column with the **mean**
- **Filled** missing values in the `Embarked` column with the **mode**

### 3️⃣ Exploratory Data Analysis (EDA)
- Visualized key relationships using **Seaborn bar plots**
- Analyzed survival rates based on:
  - **Gender** (`Sex`)
  - **Passenger Class** (`Pclass`)
  - **Embarkation Port** (`Embarked`)

### 4️⃣ Feature Engineering & Encoding
- Converted **categorical columns** (`Sex`, `Embarked`) into **numerical values**
  - Example: Male → 0, Female → 1
- **Removed irrelevant columns**: `PassengerId`, `Name`, `Ticket` which do not contribute to prediction

### 5️⃣ Data Splitting
- Divided the dataset into:
  - **Training set**: 80%
  - **Testing set**: 20%
- Used `train_test_split` from **Scikit-learn**

### 6️⃣ Model Building & Evaluation
- Built a **Logistic Regression model** using `sklearn.linear_model`
- Trained the model on the training set
- Predicted on the testing set
- Evaluated the model using **accuracy** as the key metric

## ✅ Final Outcome

A fully functional **Logistic Regression model** that can effectively predict whether a passenger survived the Titanic disaster based on relevant features such as age, gender, class, and embarkation port.

---

## 💡 Tools & Technologies Used
- **Python**
- **Pandas** – data manipulation
- **NumPy** – numerical operations
- **Seaborn & Matplotlib** – visualization
- **Scikit-learn** – model building and evaluation

---

## 📈 Results & Insights

- Female passengers had a higher survival rate
- Passengers in higher classes were more likely to survive
- Embarkation port also influenced survival likelihood

---

## 📁 Folder Structure (Optional)
```bash
titanic-logistic-regression/
├── data/
│   └── train.csv
├── notebook/
│   └── titanic_model.ipynb
├── README.md
└── requirements.txt
