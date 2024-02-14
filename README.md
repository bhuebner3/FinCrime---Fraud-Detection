# FinCrime-Fraud-Detection

## Overview
This project focuses on analyzing a synthetic dataset of customer card transactions to generate meaningful business insights and develop a fraud detection model. The dataset is divided into training and test sets (too large for github), with the training set used for analysis and model training and the test set for evaluating the model's performance.

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
- **Data Preparation**: Analyze and preprocess data for optimal model performance.
- **Exploratory Data Analysis**: Visualize and explore data to find patterns related to fraud.
  Insights were gained during this step, such as the different distributions of transaction amounts between frauds and non frauds.

  ![trans_dist](https://github.com/bhuebner3/FinCrime---Fraud-Detection/assets/73898316/10cd787a-280b-4fb7-be7b-6bc5ec711256)

  ![Dist of Trans Amounts](/repository/FinCrime---Fraud-Detection/trans_dist.png?raw=true "Dist of Trans Amounts")
- **Model Development**: Use machine learning algorithms to predict fraud.
- **Evaluation**: Assess model performance with appropriate metrics.

## Tools and Libraries
- Pandas, NumPy, Matplotlib, Seaborn for data manipulation and visualization.
- LightGBM, Scikit-learn for model building and evaluation.
- Other custom utilities as needed for specific analyses.

## Project Structure
1. **Introduction**: Overview and objectives.
2. **Data Exploration and Cleaning**: Insights into the dataset and preparation steps.
3. **Feature Engineering**: Techniques used to create meaningful variables.
4. **Model Training and Evaluation**: Approach, results, and performance metrics.
5. **Insights and Business Recommendations**: Key findings and potential product or process improvements.
6. **Future Work**: Ideas for further analysis and model enhancement.

## Conclusion
This project aims to leverage data analysis and machine learning to enhance fraud detection capabilities, providing actionable insights for improving customer transaction security and enhancing the overall user experience.

