# Myntra Apparel Data Analysis

Project Overview

This project involves analyzing a dataset from Myntra, a leading online fashion retailer. The dataset contains information about various apparel items, including their pricing, discount offers, ratings, and available sizes. The objective is to clean the dataset, perform a series of analyses, and derive meaningful insights for decision-making.

Problem Statement
As a data analyst working at Myntra, the management has tasked you with analyzing the dataset to gain insights into the following areas:

Pricing
Discounts
Ratings
Available sizes
Project Structure
Dataset
The dataset consists of various columns such as:

Product ID: Unique identifier for each product.
Brand: The brand name of the apparel item.
Original Price: The original listed price of the product.
Discount Price: The price after the discount.
Discount Offer: A mix of percentage and flat Rs. discounts, such as "50% OFF", "Rs. 100 OFF", etc.
Rating: User rating for the product.
SizeOption: Available sizes for the product (M, L, XL, etc.).
You can download the dataset from the following link.

Tasks
A. Data Cleaning and Preparation
Remove Duplicates: Check for duplicate rows in the dataset and remove them to ensure data integrity.
Standardize the DiscountOffer Column: Convert all values in the "Discount Offer" column into a uniform percentage-based format (e.g., converting "Rs. 100 OFF" into a corresponding percentage).
Handle Null Values:
Fill in the missing values in the "DiscountPrice" column using the average discount price for that product category, only if both "DiscountPrice" and "DiscountOffer" are null.
Replace null values in the "SizeOption" column with "Not Available".
B. Data Analysis
Average Original Price: Calculate the overall average original price for products with ratings greater than 4.
Count High Discounts: Count the number of products with a discount greater than 50%.
Count Available Size M: Count the number of products available in size "M".
Create a Discount Category: Add a new column to label products as "High Discount" if the discount is greater than 50%, and "Low Discount" otherwise.
C. Data Retrieval and Lookup
VLOOKUP/XLOOKUP: Find the product brand, price, and rating for the product with Product ID "11226634".
INDEX/MATCH: Retrieve the "DiscountPrice" for the product with Product ID "6744434" using INDEX and MATCH.
Nested Lookup: Use a nested XLOOKUP to retrieve any column’s detail based on the product's ID.


Here’s a sample README.md file that you can use for your GitHub project:

Myntra Apparel Data Analysis
Project Overview
This project involves analyzing a dataset from Myntra, a leading online fashion retailer. The dataset contains information about various apparel items, including their pricing, discount offers, ratings, and available sizes. The objective is to clean the dataset, perform a series of analyses, and derive meaningful insights for decision-making.

Problem Statement
As a data analyst working at Myntra, the management has tasked you with analyzing the dataset to gain insights into the following areas:

Pricing
Discounts
Ratings
Available sizes
Project Structure
Dataset
The dataset consists of various columns such as:

Product ID: Unique identifier for each product.
Brand: The brand name of the apparel item.
Original Price: The original listed price of the product.
Discount Price: The price after the discount.
Discount Offer: A mix of percentage and flat Rs. discounts, such as "50% OFF", "Rs. 100 OFF", etc.
Rating: User rating for the product.
SizeOption: Available sizes for the product (M, L, XL, etc.).
You can download the dataset from the following link.

Tasks
A. Data Cleaning and Preparation
Remove Duplicates: Check for duplicate rows in the dataset and remove them to ensure data integrity.
Standardize the DiscountOffer Column: Convert all values in the "Discount Offer" column into a uniform percentage-based format (e.g., converting "Rs. 100 OFF" into a corresponding percentage).
Handle Null Values:
Fill in the missing values in the "DiscountPrice" column using the average discount price for that product category, only if both "DiscountPrice" and "DiscountOffer" are null.
Replace null values in the "SizeOption" column with "Not Available".
B. Data Analysis
Average Original Price: Calculate the overall average original price for products with ratings greater than 4.
Count High Discounts: Count the number of products with a discount greater than 50%.
Count Available Size M: Count the number of products available in size "M".
Create a Discount Category: Add a new column to label products as "High Discount" if the discount is greater than 50%, and "Low Discount" otherwise.
C. Data Retrieval and Lookup
VLOOKUP/XLOOKUP: Find the product brand, price, and rating for the product with Product ID "11226634".
INDEX/MATCH: Retrieve the "DiscountPrice" for the product with Product ID "6744434" using INDEX and MATCH.
Nested Lookup: Use a nested XLOOKUP to retrieve any column’s detail based on the product's ID.
Key Formulae
Formula to Convert Rs. X OFF to % OFF:
excel
Copy code
=IF(AND(ISNUMBER(SEARCH("Rs", J2)), ISNUMBER(I2)), 
    TEXT((VALUE(MID(J2, FIND("Rs", J2) + 2, FIND(" OFF", J2) - FIND("Rs", J2) - 2)) / I2) * 100, "0.00") & "% OFF", 
    IF(ISNUMBER(SEARCH("%", J2)), 
        TEXT(LEFT(J2, FIND("%", J2) - 1), "0") & "% OFF", 
        "No Discount")
)
This formula converts flat Rs. discounts into a percentage based on the original price.

Formula to Handle Missing Discount Prices:
excel
Copy code
=IF(AND(ISBLANK(DiscountPrice), ISBLANK(DiscountOffer)), AVERAGEIF(CategoryColumn, ProductCategory, DiscountPriceColumn), DiscountPrice)
This formula replaces missing discount prices with the average discount price for that specific category.

Tools Used
Microsoft Excel: Primary tool for data cleaning, analysis, and formula-based operations.
PowerPoint/Canva: For presenting insights derived from the data analysis.
GitHub: Repository for project documentation and sharing the work.
Project Submission
The final project includes:

A cleaned dataset.
A PowerPoint/Canva presentation with well-designed slides showcasing key findings.
Insights and answers to each question posed in the problem statement.
Instructions for Running the Project
Download the dataset from the provided link.
Follow the steps for data cleaning, preparation, and analysis as outlined in this README.
Use Excel to apply the provided formulas and perform the necessary analyses.
Present the results in a visually appealing deck using PowerPoint, Canva, or any other tool of your choice.
Export the final presentation as a PDF and submit it.

Conclusion
This project demonstrates the end-to-end process of cleaning a real-world dataset and performing meaningful analysis to derive actionable insights. It highlights the importance of data preparation, thoughtful analysis, and clear presentation for decision-making.
