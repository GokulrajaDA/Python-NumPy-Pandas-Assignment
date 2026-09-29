# 📊 Data Analytics: NumPy & Pandas Analysis

> A comprehensive hands-on assignment focusing on numerical computing with NumPy and structured data analysis with Pandas using real-world temperature and transaction datasets.

## 📌 Overview

This assignment is part of the **Data Analytics (DA) Module-5** curriculum. It demonstrates the practical application of Python's core data analysis libraries:

- **NumPy** for efficient numerical operations and multi-dimensional array handling
- **Pandas** for data manipulation using Series and DataFrame

Two real-world scenarios are covered:
1. **Temperature Analysis** (2 weeks data) - Array operations
2. **Retail Transaction Analysis** (10 transactions) - Business data exploration

## 🎯 Objectives

- Work with NumPy arrays for numerical computations
- Use Pandas Series and DataFrame for data manipulation
- Apply indexing, slicing, filtering, and aggregation techniques
- Perform real-world data handling and derive business insights
- Understand data properties: shape, dtype, size, info, describe

## 🧪 Tasks Covered

### Part A: NumPy Array Operations - Temperature Data

| Task | Description | Key Methods |
| :--- | :--- | :--- |
| **1D Array** | Create `temperatures_w1` for Week 1 | `np.array()` |
| **Inspection** | Check shape, dtype, size | `.shape`, `.dtype`, `.size`, `.ndim` |
| **Operations** | Celsius to Fahrenheit, Max/Min/Mean | `* 9/5 + 32`, `np.max()`, `np.mean()` |
| **Slicing** | First 3 days, Weekend, Middle 3 days | `arr[:3]`, `arr[-2:]`, `arr[2:5]` |
| **2D Array** | Create 2-week matrix `temperatures` | `np.array([[],[]])` |
| **2D Slicing** | Extract week-wise & weekends | `arr[0]`, `arr[:, -2:]` |

### Part B: Pandas Series - Student Marks

- Created Series `marks` with custom index `Rank1` to `Rank5`
- **Indexing:** `iloc[0]` for position, `loc['Rank1':'Rank3']` for label slicing
- **Filtering:** Boolean mask `marks > 90`
- **Manipulation:** Modified Rank1 to 100, dropped Rank5, computed CGPA as `marks/10`

### Part C: Pandas DataFrame - Transaction Analysis

- Created DataFrame `transactions` with 10 records (TransactionID, ProductCategory, Region, Amount)

**Exploration:**
```python
df.head(), df.tail(), df.shape, df.columns, df.dtypes, df.info()
df[['ProductCategory','Amount']]
df.iloc[:, -3:]
df[(df['Region']=='North') & (df['Amount']>200)]
df['ProductCategory'].value_counts()
df['Region'].unique()
df.groupby('Region')['Amount'].mean()

Manipulation:
Updated Amount for TransactionID 102 → 165
Added Discount column = 10% of Amount
Removed row TransactionID 109
Deleted Discount column

🛠️ Tech Stack
Language: Python 3.11
Libraries:
numpy - Numerical computing
pandas - Data manipulation
Environment: Google Colab / Jupyter Notebook

📂 Repository StructurejavascriptModule-5-Numpy-Pandas/
│
├── Module_5_Numpy_Pandas.ipynb # Main Colab/Jupyter Notebook with outputs
├── analysis.py # Standalone Python script
├── data/
│ ├── temperatures.csv # (Optional) Temperature dataset
│ └── transactions.csv # (Optional) Transaction dataset
├── screenshots/ # Output screenshots
├── README.md # Documentation
└── requirements.txt # Dependencies

🚀 How to Run
1. Clone the Repository
bash
git clone https://github.com/yourusername/Module-5-Numpy-Pandas.git
cd Module-5-Numpy-Pandas2.
Install Dependencies
bash
pip install -r requirements.txt
# or
pip install numpy pandas jupyter3.

Run in Jupyter / Colab
bash
jupyter notebook Module_5_Numpy_Pandas.ipynb
Or upload the .ipynb file directly to Google Colab

📊 Key Insights & Results
Temperature Analysis:
Week 1 Avg: 23.54°C (74.37°F), Max: 26.1°C, Min: 20.8°C
Weekend temps are cooler than weekdays - useful for energy consumption prediction
Transaction Analysis:
Top Category: Electronics (4 transactions)
Top Region by Avg Amount: East Region (₹375 avg)
Filter Result: North region with Amount>200 has 3 high-value transactions
Demonstrates real business query capability

📈 Learning Outcomes
Mastered NumPy array creation, properties, and vectorized operations
Understood difference between loc (label-based) vs iloc (position-based)
Learned data filtering, grouping, and aggregation for business intelligence
Hands-on with data cleaning and transformation workflows

📝 Deliverables
Jupyter Notebook with well-commented code and outputs
Clean, formatted display using pandas
Google Drive link with View access enabled
Professional GitHub README[x]
