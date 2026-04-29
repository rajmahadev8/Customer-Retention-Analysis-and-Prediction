# Customer Retention Analysis and Prediction

This project focuses on analyzing customer churn behavior and building a machine learning model to predict whether a customer is likely to leave a service. It combines exploratory data analysis, preprocessing, feature engineering, and classification modeling to generate actionable business insights.

## Project Overview

Customer churn is a major business problem because losing existing customers often costs more than retaining them. This project analyzes customer characteristics and service usage patterns to identify churn drivers and build a predictive model for customer retention strategies.

## Objective

The main goals of this project are:

- Analyze customer data to understand churn behavior.
- Identify important factors influencing customer retention.
- Build a machine learning model to predict churn.
- Generate business insights that can support retention strategies.

## Dataset

The project uses the **Customer Churn Dataset** from Kaggle, combining the provided training and testing files into a single dataset before performing a fresh split for modeling. The combined dataset contains **505,206 rows** and includes customer demographics, service usage, payment behavior, subscription details, and churn labels.

### Features used

- CustomerID
- Age
- Gender
- Tenure
- Usage Frequency
- Support Calls
- Payment Delay
- Subscription Type
- Contract Length
- Total Spend
- Last Interaction
- Churn

> Note: `CustomerID` was removed during preprocessing because it is not useful for prediction.

## Workflow

### 1. Data Loading and Preparation
- Combined training and testing CSV files into one dataset.
- Removed `CustomerID` as a non-predictive identifier.
- Renamed columns into a cleaner lowercase format.
- Dropped the single missing-value row from the dataset.

### 2. Exploratory Data Analysis
- Performed univariate analysis using histograms, pie charts, bar plots, and boxplots.
- Examined basic dataset statistics and class distribution.
- Generated a correlation heatmap to inspect relationships between numerical features and churn.

### 3. Feature Engineering and Encoding
- Applied **Label Encoding** to categorical variables such as gender and subscription type.
- Applied **One-Hot Encoding** to contract length because EDA suggested monthly contracts show significantly higher churn.

### 4. Model Training
- Split the processed dataset into training and testing sets using `train_test_split`.
- Trained a **Decision Tree Classifier** with `max_depth=10` and `random_state=42`.

### 5. Model Evaluation
- Evaluated the model using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix
  - Classification Report

## Model Performance

The Decision Tree model achieved an **accuracy of 93.22%** on the test set.

### Classification summary
- Class `0` precision: **0.86**
- Class `0` recall: **0.99**
- Class `0` F1-score: **0.92**
- Class `1` precision: **0.99**
- Class `1` recall: **0.90**
- Class `1` F1-score: **0.94**

## Key Insights

The notebook highlights several churn-related business insights:

- Customers with frequent support calls tend to show higher churn risk.
- Short-term contracts are more likely to churn.
- Subscription type plays an important role in customer retention.

These findings can help businesses design targeted interventions for at-risk customers.

## Tech Stack

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Project Structure

```bash
.
├── MiniProject_WiSe2025_CustomerRetentionAnalysisAndPrediction_RajMahadevwala.ipynb
├── customerchurndataset-training-master.csv
├── customerchurndataset-testing-master.csv
└── README.md
```

## How to Run

1. Clone this repository:
```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

2. Install the required dependencies:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

3. Open the notebook:
```bash
jupyter notebook
```

4. Run the notebook:
- Open `MiniProject_WiSe2025_CustomerRetentionAnalysisAndPrediction_RajMahadevwala.ipynb`
- Execute the cells step by step.

## Future Improvements

- Try ensemble methods such as **Random Forest** or **XGBoost** for potentially better performance.
- Apply cross-validation and hyperparameter tuning.
- Add more temporal and behavioral features for improved churn prediction.

## Conclusion

This project demonstrates how machine learning can be used to predict customer churn and support data-driven customer retention strategies. By combining data analysis with predictive modeling, businesses can proactively identify churn risks and take action to improve customer loyalty.

## Author

**Raj Mahadevwala**  
Data Science Graduate Student  
TU Braunschweig, Germany

- LinkedIn: [https://www.linkedin.com/in/raj-mahadevwala-9549111ba/](https://www.linkedin.com/in/raj-mahadevwala-9549111ba/)
- GitHub: [https://github.com/rajmahadev8](https://github.com/rajmahadev8)
