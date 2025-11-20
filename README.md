Titanic Dataset – Exploratory Data Analysis (EDA)

This repository contains the complete Exploratory Data Analysis (EDA) performed on the Titanic Dataset as part of Task 5.
The goal of this project is to understand the dataset, analyze important survival factors, perform visualizations, and prepare the data for further modeling.

🔍 Project Overview

This project explores the Titanic dataset to identify patterns that influenced passenger survival.
The analysis includes:

Dataset loading & inspection

Handling missing values

Univariate, bivariate, and multivariate analysis

Visualizations (histograms, boxplots, countplots, KDE, heatmap, pairplot)

Feature engineering

Exporting the cleaned dataset

📁 Files in this project
task_5.py                 # Python/Colab script with full EDA code
train.csv                 # Titanic dataset (uploaded manually in Colab)
cleaned_titanic.csv       # Exported cleaned dataset
screenshots/              # Visual output images (optional)
README.md                 # Documentation file

🧠 Steps Performed in the EDA
1️⃣ Import Libraries

Used Python libraries:

NumPy

Pandas

Matplotlib

Seaborn

These enable data manipulation and visualization.

2️⃣ Upload & Load Dataset

The dataset (train.csv) is uploaded using:

from google.colab import files
uploaded = files.upload()
df = pd.read_csv(...)

3️⃣ Initial Data Exploration

Checked:

Shape of dataset

Column types

Missing values

Summary statistics

Functions used:

df.head()

df.info()

df.describe()

4️⃣ Missing Value Analysis

Generated a detailed missing value table showing:

Count

Percentage

Visual inspection helped identify major missing columns (Age, Cabin, Embarked).

5️⃣ Univariate Analysis
Numerical Columns:

Age

Fare

SibSp

Parch

Techniques used:

Histograms

KDE plots

Boxplots

Categorical Columns:

Survived

Sex

Pclass

Embarked

Technique:

Countplots

6️⃣ Bivariate Analysis

Examined survival relationships with:

Sex

Pclass

Embarked

Using:

pd.crosstab(..., normalize='index')


Visuals used:

Countplot with hue

KDE plots

Boxplots

7️⃣ Multivariate Analysis
Pairplot

A seaborn pairplot was created for major numerical features grouped by survival.

Correlation Heatmap

Generated using:

sns.heatmap(df.corr(...), annot=True)


This shows relationships between features like:

Fare & Pclass

Age & Survival (weak correlation)

🛠️ Feature Engineering

To prepare data for modeling:

Filled Embarked with mode

Filled missing Age and Fare with medians

Extracted passenger Title from Name

Created HasCabin (0/1)

Extracted cabin deck letter

Converted categorical columns to dummy variables

📝 Exported File

A cleaned version of the dataset is exported as:

cleaned_titanic.csv


Using:

df.to_csv("cleaned_titanic.csv", index=False)

📊 Key Insights from Analysis

Females had significantly higher survival rates than males

1st class passengers survived the most

Passengers with higher fares had higher survival probability

Children had a better chance of survival

Cabin information was mostly missing, but passengers with cabins generally survived more

🔧 Technologies & Libraries Used

Python

NumPy

Pandas

Seaborn

Matplotlib

Google Colab

▶️ How to Run This Project

Open Google Colab

Upload the file task_5.py or copy its code

Upload train.csv when prompted

Run cells from top to bottom

Download cleaned_titanic.csv

