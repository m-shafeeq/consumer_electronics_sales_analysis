# Consumer Electronics Sales Analysis

Exploratory data analysis of 9,000 consumer electronics sales records to find out what drives a customer's **intent to purchase**.

Built by **Muhammad Shafeeq** as the major project for the VOIS Data Visualization course.

## Problem Statement

Brands sell several product types across several brands, but it is unclear which factors actually influence whether a customer intends to buy. Raw records mixing price, age, gender, purchase frequency and satisfaction are hard to interpret without visual analysis. This project explores the data to identify the real drivers of purchase intent.

## Dataset

`consumer_electronics_sales_data.csv` has 9,000 rows and 9 columns, with no missing values.

| Column | Description |
|---|---|
| ProductID | Unique product identifier |
| ProductCategory | Laptops, Smartphones, Smart Watches, Tablets, Headphones |
| ProductBrand | Samsung, HP, Sony, Apple, Other Brands |
| ProductPrice | Price (about 100 to 3,000) |
| CustomerAge | Age (18 to 69) |
| CustomerGender | 0 or 1 |
| PurchaseFrequency | Number of purchases (1 to 19) |
| CustomerSatisfaction | Rating from 1 to 5 |
| PurchaseIntent | Target: 0 = no, 1 = yes (56.6% are 1) |

## Tech Stack

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Jupyter / Google Colab

## Analysis Steps

1. Load the CSV and inspect it with `head()` and `describe()`
2. Check for missing values (none found)
3. Univariate analysis: category, brand and age distributions
4. Bivariate analysis: price vs intent, satisfaction vs intent, satisfaction by category, purchase frequency by gender
5. Multivariate analysis: pairplot and correlation heatmap

## Key Findings

- **Satisfaction matters.** Customers rating 4 or 5 show about 84% purchase intent, against about 38% for ratings of 1 to 3.
- **Gender and age are strong signals.** Intent is about 81% for gender 1 vs 31% for gender 0. Customers under 30 show about 24% intent vs about 68% for older groups.
- **Price does not drive intent.** Average price is about 1,515 for buyers and 1,544 for non-buyers.
- **Category and brand matter little.** Every category averages about 3.0 satisfaction, and intent stays between 54% and 59% across categories and brands.
- **Purchase frequency is nearly identical by gender** (about 10.1 vs 10.0).

Correlation with PurchaseIntent: gender 0.50, satisfaction 0.39, age 0.29, price -0.02, purchase frequency about 0.



## Repository Structure

```
.
├── consumer_electronics_sales_analysis_prediction.ipynb   # analysis notebook
├── consumer_electronics_sales_data.csv                    # dataset
├── images/                                                # charts used in this README
└── README.md
```


## Future Scope

- Train Logistic Regression, Random Forest and XGBoost models to predict purchase intent
- Segment customers with clustering (for example K-Means)
- Build interactive Power BI or Tableau dashboards
- Add time, region and revenue data, and deploy as a Streamlit app

## Author

**Muhammad Shafeeq**
