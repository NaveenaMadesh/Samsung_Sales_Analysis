# Samsung Global Product Sales - EDA Project

## About this project
This is a Data Analyst portfolio project where I analyzed Samsung's global product sales data to find useful patterns and insights using Python. I did this project on my own as part of preparing to apply for Data Analyst roles, so the whole process was - cleaning, analysis, visualization and observations - is done by me from scratch.

## Dataset
I picked this dataset from Kaggle: [Samsung Global Product Sales Dataset](https://www.kaggle.com/datasets/ashyou09/samsung-global-product-sales-dataset)

It has 15,500 rows and 28 columns, covering sales from 2021 to 2024 across different countries, regions, product categories and customer types.

## Tools used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Statsmodels (for mosaic plot)

## What I did

**1. Data Quality Check**
- Checked the shape of the data, datatypes of each column
- Found null values in storage, previous_device_os and customer_rating columns
- Checked for duplicate rows (none found)
- Checked outliers in numeric columns using boxplot
- Verified there are no negative values in price/revenue/units columns

**2. Feature Selection**
Created a new dataframe with only the columns needed for analysis, removed currency related columns since I was already working with the USD columns.

**3. Univariate, Bivariate and Multivariate Analysis**
- Unit price distribution and its relation with customer age group, storage and discount over quarters
- Units sold and revenue with respect to category, region, sales channel and customer segment
- Customer rating for each category
- Return and exchange status for each category

**4. Time Series Analysis**
Checked units sold and revenue year over year and quarter over quarter to find any seasonal pattern.

## Insights I found

- Most customers buy products around the $200 price range, no big difference between age groups in terms of price preference
- Discount percentage stays more or less same across quarters, so discount doesn't seem to depend on time
- Galaxy S and Accessories sold the most, Galaxy Buds is the lowest performing category
- Europe and Asia are the top regions by units sold (around 12,500 and 10,700 units), way more than other regions
- All sales channels perform almost similarly, Corporate/B2B slightly ahead
- Individual customers bought the most units, followed by Government and Business
- Units sold increased from 2021 to 2022 but dropped after that
- Unit price went up from 2021 to 2023 then dropped
- Sales are usually high in Q2 (April-June) and low in Q3 (July-September) - looks like a seasonal pattern
- Revenue grew steadily from 2021 to 2023 then dropped suddenly
- Galaxy S and Smart TV generate the highest revenue
- Samsung Store is the channel generating the most revenue
- Government and Individual segments contribute the most to revenue
- Customer rating is good overall, mostly above 3.7 out of 5 for all categories
- Galaxy S and Accessories have higher exchange/return rates compared to other categories, even though they are top sellers - could mean a quality issue or mismatch with customer expectations

## What can be done based on this
1. Find out why revenue and units sold dropped after 2023 - whether it's because of price increase, region issue or category issue
2. Galaxy Buds needs better marketing since its sales are low compared to others
3. Check why Galaxy S and Accessories have more returns/exchanges even though they sell the most, maybe a quality check is needed
4. Since Q2 has high sales, planning stock and offers around that time could help, also need to find ways to boost Q3 sales

## About the null values
I didn't drop the null values from storage and customer_rating columns directly from the whole dataset because that would also remove other useful data present in those rows. Also, while finding average rating using describe() and mean(), pandas automatically skips the null values, so the average is correct without doing anything extra.

## Files in this repo
- `samsung_global_sales_dataset.csv` - the dataset used for this analysis
- `Sales_Analysis.ipynb` - the full notebook with code, visualizations and observations
- `README.md` - this file

## How to run this project
1. Clone or download this repository (the dataset `samsung_global_sales_dataset.csv` is already included)
2. Install the required libraries:
   ```
   pip install pandas numpy matplotlib seaborn statsmodels
   ```
3. Open `Sales_Analysis.ipynb` in Jupyter Notebook and run all the cells
