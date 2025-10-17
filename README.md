# customer-category-clustering
Customer Segmentation Using RFM Analysis and K-Means Clustering
Project Overview
This project performs Customer Segmentation using the RFM (Recency, Frequency, and Monetary) model combined with K-Means Clustering.
The main goal is to group customers based on their purchasing behavior — helping businesses understand and target different customer categories more effectively.
What is RFM Analysis?
RFM stands for:
Recency (R): How recently a customer made a purchase.
Frequency (F): How often a customer makes purchases.
Monetary (M): How much money a customer spends.
By combining these factors, we can identify loyal customers, occasional buyers, and inactive ones, allowing for better marketing decisions.
Steps Followed
Step 1: Data Preprocessing
Loaded and cleaned the dataset.
Removed missing or invalid CustomerID entries.
Converted InvoiceDate to a valid datetime format.
Step 2: RFM Feature Engineering
Created new columns for:
Recency: Days since last purchase.
Frequency: Number of transactions per customer.
Monetary: Total spending per customer.
Step 3: Feature Scaling
Scaled the RFM features using StandardScaler so that all values are on a similar scale before clustering.
Step 4: Choosing Optimal Number of Clusters (k)
Used the Elbow Method and Silhouette Score to determine the best number of clusters.
The optimal value of k = 4 was selected.
Step 5: Model Training with K-Means
Applied K-Means clustering to group customers into 4 segments.
Assigned cluster labels to each customer.
Step 6: Cluster Profiling & Visualization
Compared cluster averages to understand each group’s characteristics.
Visualized results using:
3D scatter plots for RFM clusters.
Boxplots and pairplots for feature relationships.
📊 Cluster Insights
Cluster	Recency	Frequency	Monetary	Description
0	42.70	3.68	1,359.05	Regular customers with moderate spending
1	247.08	1.55	480.62	Dormant or low-value customers
2	6.38	82.54	127,338.31	Top VIP customers (recent, frequent, and high spenders)
3	14.50	22.33	12,709.09	Active customers with consistent purchases
Tech Stack
Python
Pandas, NumPy – Data manipulation
Matplotlib, Seaborn – Data visualization
Scikit-Learn – Scaling and clustering
How to Run This Project
Step 1: Clone the Repository
git clone https://github.com/yourusername/customer-segmentation-rfm.git
cd customer-segmentation-rfm
Step 2: Install the Required Libraries
Make sure you have Python installed (version 3.8 or later), then run:
pip install -r requirements.txt

If you don’t have a requirements.txt file, you can install manually:
pip install pandas numpy matplotlib seaborn scikit-learn
Step 3: Run the Notebook or Script
If you’re using Jupyter Notebook:
jupyter notebook

Then open the .ipynb file and run the cells in order.
Or, if you’re using a Python script:
python customer_segmentation.py
Step 4: View Results
After execution, visualizations and cluster summaries will appear, showing insights from the RFM analysis and K-Means segmentation.
🚀 Future Improvements
Automate RFM updates for real-time segmentation.
Compare performance with Hierarchical Clustering and DBSCAN.
Build an interactive Streamlit dashboard for easy visualization.
👨‍💻 Author
Macnelson Chibuike
📧 mcibuike6@gmail.com
🔗 linkedin.com/in/macnelson-chibuike-b9126b292
