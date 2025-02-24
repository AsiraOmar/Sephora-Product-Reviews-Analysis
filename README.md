# **Sephora Data Analysis – Business Insights & ETL Implementation**

## Link to Large files: [Folder](https://drive.google.com/drive/folders/14_A7uznoAyWU44rxQ26U1LE1wv1qS3hf?usp=drive_link)

[Sephora database as a BAK file](https://drive.google.com/file/d/1gFCVEuep2Sy83682liob-S_7kSmv3J1L/view?usp=drive_link)

[Alteryx Workflow](https://drive.google.com/file/d/1MgxNnT9HJAYTXaxpplUb0OPNFhtgURIK/view?usp=drive_link)

[Fact and Dimension Creation - ER](https://drive.google.com/file/d/1O_9NK6IxLpCX7gX8qXyTJAamXiLlZkCL/view?usp=drive_link)

[SQL Queries](https://drive.google.com/file/d/1fxlurR_TOp9WI4AMtqB4zKtjXPpKq23q/view?usp=drive_link)

[Pyspark queries](https://drive.google.com/file/d/1zeiy0WjL_yNx5GKQ21MHCdUUD9Q-NpIa/view?usp=drive_link)

[Power BI dashboard](https://drive.google.com/file/d/1Y_Ng7C4SeupW55Fa_k11p-5biV83Ee72/view?usp=drive_link)


## **Project Overview**
This project analyzes customer reviews and product performance using the **Sephora Products and Skincare Reviews** dataset from Kaggle. The goal is to extract meaningful business insights that can help Sephora optimize inventory management, enhance customer experience, and improve product recommendations.

## **Business Problem**
Sephora, a global beauty retailer, offers thousands of products across various brands. Customer engagement and product popularity are key metrics in determining business success. The project aims to answer key questions such as:
- How can Sephora leverage customer feedback to optimize inventory?
- What are the most-loved and least-loved products?
- How do pricing, stock availability, and product exclusivity impact customer sentiment?

## **Technologies Used**
- **SQL Server Management Studio (SSMS)** – Database setup, data cleaning, transformation, and OLAP Cube modeling.
- **Alteryx** – ETL (Extract, Transform, Load) process for structuring data, aggreagtion and calculated fields.
- **Power BI** – Visualization and dashboard creation for insights.
- **SSAS in VS Code and Pyspark** – SQL scripting and data manipulation.
- **Kaggle** – Data source for Sephora product reviews.

## **Project Workflow**
### 1. **Data Cleaning (SSMS)**
- Creating the database in SSMS
- Setting datatypes for different columns
- Checking for missing values and inconsistencies
- Identifying  duplicate review entry of same author for same product
- Set a **composite primary key** (`author_id`, `product_id`) for review tables.

### 2. **ETL Processing (Alteryx)**
- Extracted data from multiple SQL tables: `SephoraProductReviews`, `ProductInfo`, and `CustomerInfo`.
- Filtered out null values, ensured uniqueness, and merged datasets.
- Classified sentiment as **Positive, Neutral, or Negative** and products as **Top rated or Standard**.
- Stored the final cleaned data in **SQL Server** for further analysis.

### 3. **Data Analysis (SSMS)**
- Converted and standardized data types for consistency (e.g., `rating`, `is_recommended`, `submission_time`).
- Analyzed key business insights, including:
  - **Highest-rated products**
  - **Most negatively reviewed products**
  - **Impact of price on customer ratings**
  - **Product recommendation trends**
  - **Stock availability analysis**

### 4. **OLAP Cube Implementation**
- Designed an OLAP Cube with **three dimension tables** (`DimCustomer`, `DimProduct`, `DimDate`) and **one fact table** (`FactProductReviews`).
- Enabled multidimensional analysis for deep business insights.

### 5. **Power BI Visualization**
- Created interactive dashboards showcasing:
  - **Top-performing brands and products**
  - **Customer sentiment trends**
  - **Out-of-stock product analysis**
  - **Revenue estimation and engagement scores**

## **Key Findings**
- **Best-Rated Product:** *FaceGym’s Youth Reformer Firming Vitamin C Oil Serum.*
- **Most Negative Feedback:** *The Ordinary’s AHA 30% + BHA 2% Peeling Solution.*
- **Luxury vs. Budget Products:** Higher-priced products had better ratings.
- **Most Recommended Product:** *Laneige’s Lip Sleeping Mask Hydration.*
- **Stock Management Issues:** Sephora Collection’s **Cleansing & Exfoliating Wipes** was frequently out of stock.
- **Customer Satisfaction:** Achieved **72.95 engagement score**, surpassing expectations.

## **Conclusion**
The analysis provides valuable insights for **inventory optimization**, **customer sentiment improvement**, and **better business decision-making**. By leveraging **OLAP cubes, Power BI dashboards, and ETL processing**, Sephora can enhance customer engagement and sales.

