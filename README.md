# FinCrime-Fraud-Detection

## Overview
This project focuses on analyzing a synthetic dataset of customer card transactions to generate meaningful business insights and develop a fraud detection model. The dataset is divided into training and test sets (too large for github), with the training set used for analysis and model training and the test set for evaluating the model's performance.

## Tools and Libraries
- Data Manipulation and Visualization
  - Pandas
  - Numpy
  - Matplotlib
  - Seaborn
  - Scoretools (custom package for bivariate tables, etc.)
- Model Building and Evaluation
  - LightGBM
  - Scikit-learn


## Dataset
The dataset comprises approximately 1.3 million records, featuring various details about customer transactions, including transaction date and time, merchant information, amount, and the fraud flag, which serves as the target class for the fraud detection model.

### Description of Top Columns
- `index`: Unique Identifier for each row
- `trans_date_trans_time`: Transaction DateTime
- `cc_num`: Credit Card Number of Customer
- `merchant`: Merchant Name
- `is_fraud`: Fraud Flag (Target Class)

## Objectives
### Part 1: Analysis of Customer Transactions
- Become familiar with the dataset to uncover patterns and insights.
- Generate 3-5 actionable business insights with visualizations to discuss potential product improvements or modifications to the KYC process.

### Part 2: Fraud Detection Model
- Develop a machine learning model to predict fraudulent transactions.
- Evaluate the model's performance using the test dataset.
- Discuss potential next steps and improvements if given more time, including exploring other data types or modeling techniques.

## Methodology
### Data Preparation
The initial step involved loading and cleaning the dataset, focusing on handling missing values, correcting data formats, and ensuring data integrity. Notably, data types were checked and corrected, zip codes were standardized to ensure proper formatting, and transaction dates and times were converted to datetime objects for easier manipulation.

### Exploratory Data Analysis (EDA)
EDA was conducted to understand the dataset's characteristics, with a focus on identifying patterns related to fraud. I created visualizations to explore fraud trends over time, by merchant category, and across various transaction amounts. For example, key insights were derived from the distribution of transaction amounts for fraudulent versus non-fraudulent transactions.

  ![trans_dist](https://github.com/bhuebner3/FinCrime---Fraud-Detection/assets/73898316/10cd787a-280b-4fb7-be7b-6bc5ec711256)

I also found interesting interactions of variables to report as actionable insights in Part 1. An example of this is transaction amount by time of day.
![heatmap](https://github.com/bhuebner3/FinCrime---Fraud-Detection/assets/73898316/f875c4b5-1bf6-49bb-a176-f42a2872ca87)

### Feature Engineering
Significant effort was put into engineering features that capture the nuances of fraudulent transactions. This includes creating features based on transaction velocity, geographic distance between the customer and merchant, and customer behavior profiling. The use of rolling windows and the creation of velocity features highlight the dynamic nature of transaction patterns. Additionally, location-based features and customer-specific attributes like age and transaction habits were included to enrich the model's input data.

### Modeling
The model development phase was approached with a focus on handling the dataset's imbalance. LightGBM was chosen as the modeling algorithm due to its efficiency and effectiveness in dealing with large datasets and categorical features. Notably, the project emphasizes the use of Precision-Recall curves and Average Precision Score as evaluation metrics; AUC (ROC) is not suitable for the imbalanced nature of fraud detection tasks. Basic hyperparameter tuning was performed, but given more time this would be more thoroughly explored.

### Evaluation
Model evaluation was carefully conducted to account for the imbalanced dataset, focusing on precision, recall, and the average precision score rather than traditional accuracy or ROC AUC metrics. This approach is more appropriate for fraud detection, where the data is highly imbalanced. The precision-recall curve provides a visual tool for understanding the trade-off between capturing as many fraud cases as possible (recall) and maintaining a high confidence level in the predicted fraud cases (precision).


### Final Thoughts and Future Directions
The analysis concludes with reflections on the project and considerations for future work. Potential improvements include exploring anomaly detection algorithms, addressing the specific challenge of ID theft, focusing on the detection of the first fraudulent transaction to prevent further unauthorized activities, and expanding the feature set for more nuanced detection capabilities.

