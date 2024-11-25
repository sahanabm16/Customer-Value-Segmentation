# Customer Value Segmentation with RFM and K-Means Clustering

## Project Overview

This project implements customer segmentation using **RFM (Recency, Frequency, Monetary)** analysis combined with **K-Means clustering**. The goal is to categorize customers into meaningful segments, such as **high value**, **low value**, and **potentially loyal** customers, by leveraging their transactional data. These insights help businesses target specific customer segments with personalized marketing strategies.

## Dataset

The dataset used for this analysis includes customer transactions from an online retail store. The primary features include:

- **Invoice**: Invoice number of the transaction.
- **StockCode**: Unique identifier of the product.
- **Description**: Product description.
- **Quantity**: Number of units purchased.
- **InvoiceDate**: The date and time of the transaction.
- **UnitPrice**: Price per product unit.
- **Customer ID**: Unique identifier for each customer.
- **Country**: Customer's country of origin.

### Data Cleaning
- **Outliers**: Outliers were identified and removed from the dataset to ensure accurate segmentation results.
- **Missing Values**: Rows with missing `Customer ID` were handled before analysis.

## Steps Involved

1. **Data Preprocessing**: 
   - Removal of outliers to ensure that the analysis is not skewed by extreme values.
   - Cleaning the dataset by filtering out incomplete records.

2. **RFM Calculation**:
   - **Recency**: How long it has been since a customer's last purchase.
   - **Frequency**: The total number of transactions a customer has made.
   - **Monetary**: The total amount a customer has spent.

3. **Revenue Metrics Calculation**:
   In addition to RFM, several key revenue metrics are calculated for each customer:
   - **LastMonthRevenue**: Revenue generated by the customer in the last month.
   - **ThreeMonthsRevenue**: Revenue generated in the last three months.
   - **SixMonthsRevenue**: Revenue generated in the last six months.
   - **TwelveMonthsRevenue**: Revenue generated over the last twelve months.
   - **LifeTimeRevenue**: Total revenue from the customer's lifetime of purchases.

4. **K-Means Clustering**:
   - **K-Means** clustering is applied to segment the customers into 3 distinct clusters based on RFM and revenue metrics.
   - The optimal number of clusters is determined using techniques like the **elbow method**.

5. **Customer Segmentation**:
   - After clustering, the customers are grouped into three segments:
     - **High Value**: Customers with high revenue and frequent purchases.
     - **Low Value**: Customers with low engagement or spend.
     - **Potentially Loyal**: Customers who show signs of loyalty but aren't high spenders yet.

6. **Visualization**:
   - The customer segments are visualized using plots and charts to better understand their distribution and characteristics.
   - Revenue trends and customer behaviors are represented graphically.

## Results

The segmentation using K-Means provided meaningful insights into customer behavior, allowing for targeted strategies aimed at improving customer retention and boosting revenue.

## How to Run the Code

1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd <repo_folder>
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook CxValueSegmentation.ipynb
   ```

## Dependencies

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## Visualizations

- RFM distribution across different clusters.
- Revenue distribution over time for different customer segments.
- Cluster analysis based on revenue metrics.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

![image](https://github.com/user-attachments/assets/b39a6540-1611-4132-8d08-8a9162506bc7)
