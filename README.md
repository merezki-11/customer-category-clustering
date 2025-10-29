Customer Segmentation Using RFM Analysis and K-Means Clustering

Project Overview

This project performs Customer Segmentation using the RFM model (Recency, Frequency, and Monetary) combined with K-Means Clustering.
The main goal is to group customers based on their purchasing behavior and helping businesses understand and target different customer categories more effectively.

What is RFM Analysis?

RFM stands for:
Recency (R): How recently a customer made a purchase.
Frequency (F): How often a customer makes purchases.
Monetary (M): How much money a customer spends.

By combining these factors, businesses can identify: Loyal customers, Occasional buyers, and Inactive customers, hence enabling smarter marketing decisions and better customer retention strategies.

 Steps Followed
 Step !: Data Preprocessing
 - Loaded and cleaned the dataset  
 - Removed missing or invalid `CustomerID` entries  
 - Converted `InvoiceDate` to a valid datetime format  

Step 2: RFM Feature Engineering
Created new columns for:  
- **Recency:** Days since last purchase  
- **Frequency:** Number of transactions per customer  
- **Monetary:** Total spending per customer

 Step 3: Feature Scaling
 Scaled the RFM features using **StandardScaler** so that all values are on a similar scale before clustering.

 Step 4: Choosing Optimal Number of Clusters (k)
 - Used **Elbow Method** and **Silhouette Score** to find the best number of clusters  
 - Selected **k = 4** as the optimal value.
   
Step 5: Model Training with K-Means
- Applied **K-Means clustering** to group customers into 4 segments  
- Assigned cluster labels to each customer

Step 6: Cluster Profiling & Visualization
- Compared cluster averages to understand group characteristics.
- Visualized results using:
  - 3D scatter plots for RFM clusters.
  - Boxplots and pairplots for feature relationships.

Cluster Insights
| Cluster | Recency | Frequency |  Monetary  | Description                                         |
| :-----: | :-----: | :-------: | :--------: | :-------------------------------------------------- |
|  0  |  42.70  |    3.68   |  1,359.05  | Regular customers with moderate spending            |
|  1  |  247.08 |    1.55   |   480.62   | Dormant or low-value customers                      |
|  2  |   6.38  |   82.54   | 127,338.31 | Top VIP customers (recent, frequent, high spenders) |
|  3  |  14.50  |   22.33   |  12,709.09 | Active customers with consistent purchases          |

Tech Stack
| Tool                        | Purpose                |
| --------------------------- | ---------------------- |
| Python              | Programming language   |
| Pandas, NumPy       | Data manipulation      |
| Matplotlib, Seaborn | Data visualization     |
| Scikit-Learn        | Scaling and clustering |

How to Run This Project

Step 1: Clone the Repository
git clone https://github.com/merezki-11/customer-segmentation-rfm.git
cd customer-segmentation-rfm

Step 2: Install Dependencies
pip install -r requirements.txt

Step 3: Run the Notebook or Script
For Jupyter Notebook:
jupyter notebook
For Python Script:
python customer_segmentation.py

Step 4: View Results

Once executed, visualizations and cluster summaries will appear  showing clear insights from the RFM analysis and K-Means segmentation.

Future Improvements

- Automate RFM updates for real-time segmentation
- Compare performance with Hierarchical Clustering and DBSCAN
- Build an interactive Streamlit dashboard for dynamic visualization.

  Author

Macnelson Chibuike

macnelsonchibuike11@gmail.com

linkedin.com/in/macnelson-chibuike-b9126b292

github.com/merezki-11
