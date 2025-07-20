# Fraud Detection in Bank Transactions Using AI Models

## Overview
This repository contains the implementation of a fraud detection project using two datasets: `Fraud_Data.csv` (e-commerce transaction data) and `IpAddress_to_Country.csv` (IP-to-country mapping). The project is divided into three tasks:
- **Task 1**: Data cleaning, exploratory data analysis (EDA), feature engineering, and data transformation.
- **Task 2**: Model training and hyperparameter tuning to predict fraudulent transactions.
- **Task 3**: Model evaluation, comparison, and final reporting.

This repository currently includes Task 1, with future tasks to be added as the project progresses.

## Repository Structure
```
fraud_detection_task1/
├── data/
│   ├── Fraud_Data.csv
│   ├── IpAddress_to_Country.csv
├── notebooks/
│   ├── fraud_detection_task1.ipynb
├── figures/
│   ├── class_distribution.png
│   ├── correlation_heatmap.png
│   ├── purchase_value_histogram.png
│   ├── purchase_value_by_class.png
├── README.md
```

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/fraud_detection_task1.git
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
   ```
3. Ensure VS Code with the Data Wrangler extension is installed for interactive data processing.
4. Place `Fraud_Data.csv` and `IpAddress_to_Country.csv` in the `data/` folder.
5. Run the notebook:
   ```bash
   jupyter notebook notebooks/fraud_detection_task1.ipynb
   ```

## Datasets
- **Fraud_Data.csv**: Contains e-commerce transaction data with columns:
  - `user_id`, `signup_time`, `purchase_time`, `purchase_value`, `device_id`, `source`, `browser`, `sex`, `age`, `ip_address`, `class` (0=non-fraud, 1=fraud).
- **IpAddress_to_Country.csv**: Maps IP address ranges to countries with columns:
  - `lower_bound_ip_address`, `upper_bound_ip_address`, `country`.

## Task Breakdown
### Task 1: Data Preprocessing and EDA
- **Data Cleaning**: Imputed missing values, removed duplicates, and converted data types (e.g., timestamps to datetime).
- **EDA**: Conducted univariate (histograms, bar plots) and bivariate (heatmap, box plots) analyses to understand feature distributions and relationships.
- **Feature Engineering**: Created features like `hour_of_day`, `day_of_week`, `time_since_signup`, `transaction_count`, `avg_velocity`, and `country` (via IP merge).
- **Data Transformation**: Scaled numerical features, encoded categorical features, and analyzed class imbalance (ratio 9.68).
- **Outputs**: Visualizations (`class_distribution.png`, `correlation_heatmap.png`) and preprocessed data (`preprocessed_fraud_data.csv`).

### Task 2: Model Training (To Be Implemented)
- Train machine learning models (e.g., logistic regression, random forest) to predict fraud.
- Use SMOTE to handle class imbalance.
- Perform hyperparameter tuning.

### Task 3: Model Evaluation (To Be Implemented)
- Evaluate models using metrics like precision, recall, F1-score, and AUC-ROC.
- Compare model performance and select the best model.
- Generate a final report with findings.

## Running Task 1
1. Open `notebooks/fraud_detection_task1.ipynb` in Jupyter or VS Code.
2. Execute all cells to preprocess data, generate features, and create visualizations.
3. Outputs are saved in `figures/` and `preprocessed_fraud_data.csv`.

## Future Work
- Implement Task 2: Model training with SMOTE and hyperparameter tuning.
- Complete Task 3: Model evaluation and final reporting.

## Contact
For questions, contact [your-email@example.com].