# Customer-Segmentation-Using-RFM-Analysis-in-E-Commerce
Analyze e-commerce transactional data to identify high-value customers, detect trends, and optimize targeted marketing through effective customer segmentation Using Power Bi dashboard and python.
# Dataset Overview
Source: [Kaggle - E-commerce Dataset]

Size: (541909, 8)

Timeframe: 01/12/2010 to 09/12/2011
<img width="553" height="306" alt="image" src="https://github.com/user-attachments/assets/f641ce7c-77f1-4a38-8d23-e136a499a46c" />
Key Variables:
InvoiceNo: Unique transaction ID
StockCode: Unique product identifier
Description: Product description
Quantity: Number of items purchased
InvoiceDate: Timestamp of purchase
UnitPrice: Price per unit in GBP
CustomerID: Unique customer identifier
Country: Location of the customer
<img width="583" height="386" alt="image" src="https://github.com/user-attachments/assets/2a347a80-c541-4299-b8c6-465b21371eaf" />
# Data Cleaning and Preparation
1.**Handled Missing Values**  - The percentage of missing values in the CustomerID column is 24.93%.
Since the analysis will revolve around investigating customers and clustering them into categories, the missing values in the CustomerIDs were removed. 
<img width="1868" height="121" alt="image" src="https://github.com/user-attachments/assets/31bc3a98-f3b7-4d3e-83c5-a8552eb07b3a" />

2.**Removed Duplicates** - The number of duplicate rows in the dataset is 5525.
These rows were removed from the dataset.
<img width="662" height="121" alt="image" src="https://github.com/user-attachments/assets/d0d1975b-1456-4144-aea5-e99112f1f92d" />

3.**Removed Cancelled Orders** - There are  8872 rows for which the quantity is negative which can be either due to data-entry errors or return orders or cancelled orders.
If we look at the InvoiceNo for all these cases, they start with the letter ‘C’ which indicates they are cancelled orders. Thus these rows were removed from the dataset
<img width="2006" height="121" alt="image" src="https://github.com/user-attachments/assets/e75728a7-056c-4279-af76-40d037efd3a7" />

4.**Removing non-product Stock-Codes** - There are certain StockCodes which do not belong to any products. All the rows containing such StockCodes were removed. 
<img width="1524" height="56" alt="image" src="https://github.com/user-attachments/assets/0888b8e6-adfc-4019-af3f-42e3f792842f" />

<img width="513" height="231" alt="image" src="https://github.com/user-attachments/assets/4d84e334-b414-4aeb-9b81-fcdf31878780" />

# Preto Principle - Roughly 80% of outcomes stem from 20% of causes <img width="507" height="676" alt="image" src="https://github.com/user-attachments/assets/ed67105f-e3ca-44d0-9c11-abb1dc6267da" />
 26% -- customers contribute to 80% of the revenue
 21% -- products contribute to 80% of the revenue
<img width="1067" height="94" alt="image" src="https://github.com/user-attachments/assets/f92fb422-bf39-4d90-ac10-fe7f7158f35e" />
# RFM Analysis and Customer Segmentation<img width="1351" height="140" alt="image" src="https://github.com/user-attachments/assets/6ebd3e07-c669-4c19-8944-1c0c830b1416" />
What is RFM?
Recency (R): Days since last purchase
Frequency (F): Number of purchases
Monetary (M): Total spending

Customers are segmented into five equal buckets based on Recency, Frequency, and Monetary values. Each customer is ranked for each metric, assigned a score from 1 to 5, and their scores are summed to derive an overall RFM score for analysis<img width="2995" height="303" alt="image" src="https://github.com/user-attachments/assets/353ba168-adf3-4e32-bb6d-c18278d57de1" />
**customer segments based on rfm score**
<img width="716" height="443" alt="image" src="https://github.com/user-attachments/assets/e1a9fa71-4cf4-44eb-899b-3c32bc1b3828" />
# Recommendations based on customers
1- At-risk customers
2- High value customers
3- loyal customers
4- Dormant customers
