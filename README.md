# Expense Meter 
## 🚀 Introduction
Managing personal finances effectively is crucial in today's fast-paced world. The **Expense Meter** is a project designed to provide users with a clear insight into their spending habits, making it particularly useful for anyone planning major financial commitments, such as applying for loans.

## 🎯 Objective
The primary goal of the Expense Meter is to help users understand where their money goes each month, enabling better financial decisions and planning. This tool simplifies the tracking of expenses across various categories like dining out, online shopping, and utility payments, paving the way for smarter budget management.

## 💡 How It Works
- **Extract and Clean Data**: Automates the extraction of transaction details from credit card statements to ensure data accuracy and save time.
- **Categorize Expenses**: Transactions are categorized into groups such as groceries, entertainment, and utilities, which facilitates easy identification of spending trends.
- **Visualize Data**: Uses AWS Athena and Tableau to create dynamic, user-friendly dashboards that visually break down monthly expenses.

## 🔍 Impact
Expense Meter serves as more than just a tool—it's a financial companion that empowers users to:
- **Monitor Spending**: Quickly identify which categories you’re spending the most in.
- **Plan for Big Purchases**: Efficiently set aside funds for major investments.
- **Assess Loan Affordability**: Better understand your financial health before taking on debt.

## 🛠️ Built With
- **Python**: For data processing.
- **AWS S3 and Athena**: For data storage and querying.
- **Tableau**: For data visualization.

This project not only posed a fantastic technical challenge but also provided a rewarding opportunity to blend data engineering with practical financial solutions.
---

## Overview
The Expense Meter project is designed to automate the processing of credit card statements, making it easier to analyze and visualize expenditure patterns. This solution extracts data from unstructured credit card statement PDFs, cleans and categorizes the transactions, and finally, visualizes the data using a Tableau dashboard that connects to AWS Athena where the cleaned data is stored.

## Process Flow
1. **Extract Data**: Utilizing Python, the project begins by extracting data from American Express credit card statement PDFs, identifying the transaction sections within the documents.
2. **Data Cleaning**: The data undergoes a cleaning process to remove unnecessary or sensitive information such as locations, numbers, URLs, and service-specific tokens (e.g., 'AplPay').
3. **Categorization**: Transactions are categorized into various types such as Restaurants, Supermarkets, Online Streaming Platforms, etc., with a default category of 'Others' for uncategorized expenses.
4. **Upload to AWS S3**: The cleaned and processed CSV file is uploaded to an AWS S3 bucket.
5. **AWS Athena Integration**: Data stored in S3 is then queried using AWS Athena, preparing it for visualization.
6. **Tableau Dashboard**: The final step involves creating an interactive dashboard in Tableau that connects to AWS Athena, allowing for detailed visualization and analysis of the expense data.

## Detailed Steps in Jupyter Notebook
- **Reading the PDF Document**: The notebook begins by reading the American Express credit card statement PDF.
- **Transaction Extraction**: It identifies the start and end pages of transactions within the PDF.
- **Data Merging and Cleaning**: After extraction, the data is merged and cleaned, focusing on removing transaction-specific details like URLs and placeholder tokens.
- **Handling Transaction Methods**: The type of payment method for each transaction is identified (e.g., Internet, Apple Pay, Card).
- **Categorization**: Transactions are systematically categorized based on the service or product type.
- **Visualization and S3 Storage**: Lastly, the data is visualized and then sent to an AWS S3 bucket for further processing.

## Visualization
The visualization phase involves connecting Tableau to AWS Athena where the structured data allows for creating an interactive dashboard that provides insights into spending patterns and financial management.

## Conclusion
The Expense Meter project simplifies the task of financial tracking and analysis, providing a streamlined process from data extraction to visualization, leveraging powerful tools like Python, AWS Athena, and Tableau.

---

Feel free to explore the Jupyter notebook in this repository to understand more about the data extraction and cleaning processes involved in this project.
