# Myntra Apparel Data Analysis

## Project Overview
This project focuses on analyzing a dataset from **Myntra**, a popular online fashion retailer. The dataset contains details of various apparel items such as prices, discounts, ratings, and available sizes. The goal is to clean the data and extract useful insights that can aid in decision-making.

## Problem Statement
As a data analyst at Myntra, you have been asked to analyze the dataset to provide insights on pricing, discounts, ratings, and available sizes. This will help the management in making data-driven decisions.

## Project Tasks

### A. Data Cleaning and Preparation
1. **Duplicate Removal**: Remove any duplicate entries to ensure data accuracy.
2. **Standardize Discounts**: Convert all discount values (both percentage and flat Rs. discounts) into a uniform format.
3. **Handle Missing Data**:
   - Fill missing "DiscountPrice" values with the average discount price for that category if both "DiscountPrice" and "DiscountOffer" are missing.
   - Replace null values in the "SizeOption" column with "Not Available".

### B. Data Analysis
1. **Average Price for High-Rated Products**: Calculate the average original price for products with ratings higher than 4.
2. **High Discounts**: Count how many products have discounts greater than 50%.
3. **Size M Availability**: Count how many products are available in size "M."
4. **Discount Labeling**: Add a new column labeling products as "High Discount" (above 50%) or "Low Discount" (50% or below).

### C. Data Retrieval
1. **Product Lookup**: Use Excel’s VLOOKUP or XLOOKUP functions to find the brand, price, and rating of a specific product.
2. **Discount Lookup**: Use INDEX and MATCH functions to retrieve the discount price of a product.
3. **Nested Lookup**: Retrieve any product details using nested XLOOKUP based on the product ID.

## Tools Used
- **Microsoft Excel**: For data cleaning, analysis, and lookup tasks.
- **Presentation Tools**: Use PowerPoint, Canva, or any tool of your choice to present your findings.


## Conclusion
This project demonstrates the process of cleaning a real-world dataset and deriving insights for business decisions through data analysis.

