# SmartCart
# 🛒 SmartCart – Customer Segmentation & Analysis

SmartCart is a **customer analytics and segmentation project** developed using Python and machine learning techniques. The project analyzes customer demographic, purchasing, and behavioral data to identify meaningful customer groups.

The analysis includes **data preprocessing, feature engineering, outlier analysis, dimensionality reduction using PCA, and K-Means clustering** to segment customers based on their characteristics and shopping behavior.

## 📌 Project Objective

The main objective of SmartCart is to analyze customer behavior and divide customers into meaningful segments.

Customer segmentation can help understand differences in:

* Customer spending patterns
* Purchasing channels
* Income
* Age
* Number of children
* Education level
* Customer tenure
* Deal purchases
* Web, catalog, and store purchases

These segments can provide useful insights for targeted marketing and customer relationship strategies.

## 📊 Dataset

The project uses a customer dataset loaded from:

```text
smartcart_customers.csv
```

The original dataset contains:

* **2,240 customer records**
* **22 features**

The dataset includes attributes such as:

* ID
* Year of Birth
* Education
* Marital Status
* Income
* Kidhome
* Teenhome
* Customer joining date
* Recency
* Product spending
* Deal purchases
* Web purchases
* Catalog purchases
* Store purchases
* Web visits
* Complaints
* Response

## 🧹 Data Preprocessing

The project performs several preprocessing steps before applying machine learning.

### Missing Values

Missing values were identified in the dataset. The `Income` column contained missing values, which were replaced using the median income.

### Feature Engineering

Several new features were created:

* **Age** – calculated from the customer's birth year.
* **Customer_Tenure_Days** – number of days since the customer joined.
* **Total_Spending** – combined spending across product categories.
* **Total_Children** – combination of children and teenagers in the household.
* **Living_With** – simplified marital/living status.

Education categories were also grouped into broader categories such as **Undergraduate, Graduate, and Postgraduate**.

### Feature Selection

Several original columns were removed after creating the engineered features. The resulting cleaned dataset contains **2,240 records and 15 features**.

## 📈 Exploratory & Outlier Analysis

The notebook includes analysis of the customer data and visualization techniques to investigate the distribution of features and identify potential outliers.

## 🔬 Dimensionality Reduction

**Principal Component Analysis (PCA)** is used to reduce the dimensionality of the processed customer data before clustering.

This makes it easier to represent customer patterns in a lower-dimensional feature space.

## 🤖 Customer Clustering

The project uses **K-Means clustering** to group customers with similar characteristics.

The final clustering implementation uses:

```python
KMeans(n_clusters=4, random_state=42)
```

The clustering is performed on the PCA-transformed feature set.

The notebook also evaluates different values of **K (2–10)** using WCSS and silhouette scores to help determine an appropriate number of clusters.

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data manipulation and preprocessing
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Scikit-learn** – Machine learning, PCA, and K-Means clustering
* **Jupyter Notebook** – Development environment

The notebook imports Pandas, Matplotlib, and Seaborn for data analysis and visualization.

## 📂 Project Structure

```text
SmartCart/
│
├── smartcart.ipynb
├── smartcart_customers.csv
└── README.md
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Asmitaiam/SmartCart.git
```

### 2. Open the project

```bash
cd SmartCart
```

### 3. Install dependencies

```bash
pip install pandas matplotlib seaborn scikit-learn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
smartcart.ipynb
```

Make sure `smartcart_customers.csv` is present in the same project directory because the notebook loads the dataset directly from that filename.

## 🎯 Key Workflow

```text
Customer Dataset
       ↓
Data Preprocessing
       ↓
Missing Value Handling
       ↓
Feature Engineering
       ↓
Feature Selection
       ↓
Outlier Analysis
       ↓
Data Scaling
       ↓
PCA
       ↓
K-Means Clustering
       ↓
Customer Segmentation
```

## 🔮 Future Improvements

* Create detailed profiles for each customer segment
* Develop a customer-segment dashboard
* Add interactive visualizations
* Compare K-Means with other clustering algorithms
* Build a recommendation system based on customer segments
* Deploy the analysis as a web application
* Automate customer segmentation for new customer data

## 👩‍💻 Author

**Asmita Paul**

GitHub: [@Asmitaiam](https://github.com/Asmitaiam)


