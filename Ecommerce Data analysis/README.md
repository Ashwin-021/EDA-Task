# 🛒 Ecommerce Order Data Analysis

## 📌 Project Overview

This project focuses on analyzing an **Ecommerce Order Dataset** to understand customer behavior, product sales, order patterns, payment methods, discounts, and customer ratings.

The dataset contains information about orders, customers, products, prices, quantities, discounts, delivery dates, and ratings. Python and popular data analysis libraries are used to clean, explore, and visualize the data.

## 🎯 Objectives

* Analyze ecommerce order and customer data.
* Understand product and category-wise sales patterns.
* Analyze customer demographics and purchasing behavior.
* Identify commonly used payment methods.
* Study discounts and their impact on orders.
* Analyze customer ratings.
* Explore order and delivery dates.
* Generate useful insights through data visualization.

## 📂 Dataset

**Dataset Name:** `Ecommerce_Order_Test_Dataset(1).csv`

The dataset contains **101 records** and **13 columns**.

### Dataset Columns

| Column          | Description                       |
| --------------- | --------------------------------- |
| `Order_ID`      | Unique ID of each order           |
| `Order_Date`    | Date when the order was placed    |
| `Delivery_Date` | Date when the order was delivered |
| `Customer_Name` | Customer identifier               |
| `Gender`        | Customer gender                   |
| `City`          | Customer city                     |
| `Category`      | Product category                  |
| `Product`       | Product purchased                 |
| `Payment_Mode`  | Payment method used               |
| `Quantity`      | Number of products purchased      |
| `Unit_Price`    | Price of one product              |
| `Discount`      | Discount applied to the order     |
| `Rating`        | Customer rating                   |

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

## 🔍 Data Analysis

The project includes the following analysis:

### 1. Data Understanding

* Dataset shape
* Column information
* Data types
* Statistical summary
* First and last records

### 2. Data Cleaning

* Handling missing values
* Removing duplicate records
* Removing unnecessary spaces from text columns
* Standardizing categorical values
* Converting date columns into proper datetime format

### 3. Exploratory Data Analysis

The analysis explores:

* Orders by city
* Orders by gender
* Category-wise orders
* Product-wise sales
* Payment mode distribution
* Quantity purchased
* Unit price distribution
* Discount analysis
* Customer rating distribution
* Order and delivery trends

### 4. Data Visualization

Different charts are used to understand the data visually:

* Bar charts
* Count plots
* Histograms
* Pie charts
* Box plots
* Line charts
* Heatmaps

## 📊 Key Analysis Questions

Some of the questions explored in this project include:

1. Which product categories have the most orders?
2. Which cities generate the highest number of orders?
3. Which payment method is most commonly used?
4. Which products are purchased most frequently?
5. What is the distribution of customer ratings?
6. How are discounts distributed across orders?
7. Which gender has more orders?
8. What is the relationship between quantity and unit price?
9. Which products receive higher customer ratings?
10. How long does it take for orders to be delivered?

## 📁 Project Structure

```text
Ecommerce-Order-Data-Analysis/
│
├── Dataset/
│   └── Ecommerce_Order_Test_Dataset(1).csv
│
├── Notebook/
│   └── Ecommerce_Order_Data_Analysis.ipynb
│
├── Output/
│   ├── category_analysis.png
│   ├── city_analysis.png
│   ├── payment_mode_analysis.png
│   ├── rating_analysis.png
│   └── sales_analysis.png
│
└── README.md
```

## 🚀 How to Run

### Step 1: Clone the Repository

```bash
git clone <your-github-repository-url>
```

### Step 2: Open the Project

Open the project folder in **VS Code**, **Jupyter Notebook**, or **Google Colab**.

### Step 3: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### Step 4: Run the Notebook

Open:

```text
Notebook/Ecommerce_Order_Data_Analysis.ipynb
```

Run the cells step by step to perform data cleaning, analysis, and visualization.

## 📈 Expected Outcome

This project provides a clear understanding of ecommerce order data and helps identify:

* Customer purchasing patterns
* Popular products and categories
* Preferred payment methods
* City-wise order distribution
* Discount patterns
* Customer satisfaction through ratings
* Order and delivery trends


