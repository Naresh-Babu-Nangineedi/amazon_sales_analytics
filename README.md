
# Amazon Sales Data Analysis

## Project Overview
This project involves analyzing Amazon sales data using Microsoft Fabric and Power BI. The dataset provides detailed insights into Amazon sales, including SKU Code, Design Number, Stock, Category, Size, and Color, to help optimize product profitability.

## Dataset
**Amazon Sales Dataset**
- **Category**: Type of product (String)
- **Size**: Size of the product (String)
- **Date**: Date of the sale (Date)
- **Status**: Status of the sale (String)
- **Fulfilment**: Method of fulfilment (String)
- **Style**: Style of the product (String)
- **SKU**: Stock Keeping Unit (String)
- **ASIN**: Amazon Standard Identification Number (String)
- **Courier Status**: Status of the courier (String)
- **Qty**: Quantity of the product (Integer)
- **Amount**: Amount of the sale (Float)
- **B2B**: Business to business sale (Boolean)
- **Currency**: The currency used for the sale (String)

## Architecture 
![architecture](https://github.com/user-attachments/assets/6daaadc2-fc7f-42b7-8f8c-1bb028d3bf94)

## Data Processing Steps
1. **Load Data into Microsoft Fabric Lakehouse**.
2. **Create Bronze Table**.
3. **Transformations and Silver Tables**.
4. **Data Modeling**.
5. **Create Semantic Model**.

## Dashboards
1. **Sales Overview Dashboard**.
![sales_dashboard](https://github.com/user-attachments/assets/c12478f9-d260-4762-8e48-922d3363415d)

2. **SKU Management Dashboard**.
![SKU_dashboard](https://github.com/user-attachments/assets/a6ad2b90-9252-4cc0-b085-8f024bcfb0ea)


## Deployment Guide

**Prerequisites**
Microsoft Fabric workspace
F64 capacity or higher
Power BI Premium license (for Direct Lake)

Setup Steps
1. Upload Data:
bash
fabric-cli data upload --file sales_data.csv --lakehouse Sales_LH
2. Run Pipeline:
python
# Execute notebooks in sequence
notebooks/1_bronze_ingestion.py
notebooks/2_silver_cleaning.py
notebooks/3_gold_modeling.py
3. Deploy Dashboards:
Publish .pbix files to your workspace
Configure scheduled refresh
