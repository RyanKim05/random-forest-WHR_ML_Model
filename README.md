<h1>🌍 Predicting World Happiness Scores with Machine Learning</h1>

This project implements a machine learning pipeline to predict a country’s Life Ladder (a measure of life satisfaction) using socioeconomic, health, and political indicators from the World Happiness Report dataset.

The goal is to build a regression model that helps identify the most influential factors driving happiness across nations.

## **📊 Dataset**
We use the World Happiness Report (2018) Online Data (WHR2018Chapter2OnlineData.csv), which includes:

Target Variable (Label): Life Ladder (happiness score)

## **Features:**

Log GDP per capita

Social support

Healthy life expectancy at birth

Freedom to make life choices

Generosity

Perceptions of corruption

Positive affect

Negative affect

Confidence in national government

Democratic Quality

Delivery Quality

## **🧪 Machine Learning Lifecycle**
1. Problem Definition
Task: Predict Life Ladder scores from other features.

Type: Supervised Learning → Regression.

2. Data Preparation
Dropped irrelevant columns (country, year, GINI indices, etc.)

Handled missing values by imputing with the mean.

Selected 11 relevant features.

3. Modeling
Baseline Model: Random Forest Regressor (n_estimators=100).

Optimization: Used GridSearchCV with hyperparameter tuning.

4. Evaluation Metrics
Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R² Score

## **🚀 Results**
Model	MAE	RMSE	R²
Baseline RF	0.304	0.396	0.878
Tuned RF	0.306	0.400	0.876

✅ The model generalizes well, with ~88% variance explained in test data.
✅ Top predictors: GDP per capita, Social support, Perceptions of corruption.

## **📈 Visualizations**
🔹 Feature Importances
<img width="755" height="387" alt="image" src="https://github.com/user-attachments/assets/57deec76-5f51-4653-8421-f6c20590aaf3" />

🔹 Actual vs Predicted Life Ladder

<img width="568" height="424" alt="image" src="https://github.com/user-attachments/assets/68b97687-a57c-4897-9ff8-209d8b5be792" />

## **💡 Insights**
GDP per capita was the strongest predictor of life satisfaction.

Social support and political corruption also played key roles.

Model could be applied to estimate happiness in countries with incomplete data.

## **🔧 Next Steps**
Incorporate time trends using the year column.

Try other ensemble models (Gradient Boosting, XGBoost).

Improve imputation using KNN or regression instead of mean.

Extend analysis to regional comparisons.

## **⚙️ Tech Stack**
Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)

Modeling: Random Forest, GridSearchCV

Visualization: Seaborn, Matplotlib

##**📂 Project Structure**
bash
Copy
Edit
├── data/
│   └── WHR2018Chapter2OnlineData.csv
├── notebook.ipynb   # Full workflow
├── feature_importances.png
├── pred_vs_actual.png
└── README.md
