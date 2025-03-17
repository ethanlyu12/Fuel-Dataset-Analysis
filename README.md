# Fuel-Dataset-Analysis
# Project Description - Fall 2024

This document provides details about the datasets used for the group project. The datasets contain real-world fuel purchase and sales data from city gas stations. Some elements have been obfuscated to protect proprietary information.

## Data Dictionary

### `Locations.csv`
Contains gas station location details:
- **Gas Station Location**: Unique ID of the gas station
- **Gas Station Name**: Name of the gas station
- **Gas Station Address**: Address of the gas station
- **Gas Station Latitude/Longitude**: Geographical coordinates

### `Tanks.csv`
Information about gas station tanks:
- **Tank ID**: Unique identifier of each tank
- **Tank Location**: Gas station where the tank is located
- **Tank Number**: Identifier for each tank at a location
- **Tank Type**: Fuel type: `U` (Regular), `D` (Diesel), `P` (Premium)
- **Tank Capacity**: Tank capacity in liters

### `Invoices.csv`
Records fuel purchases by gas stations:
- **Invoice Date**: Date of purchase
- **Invoice ID**: Unique identifier for invoices
- **Invoice Gas Station Location**: Location of the gas station
- **Gross Purchase Cost**: Total cost in CAD
- **Amount Purchased**: Volume of fuel purchased in liters
- **Fuel Type**: Type of fuel purchased

### `Fuel_Level_Part_1.csv` and `Fuel_Level_Part_2.csv`
Fuel level tracking data:
- **Tank ID**: Identifier of the tank
- **Fuel Level**: Fuel volume remaining in liters
- **Time Stamp**: Timestamp of the fuel level reading

---

## Problem Description

Gas stations purchase fuel in bulk to meet customer demands. Inventory management affects operational efficiency and profitability. Stations must balance:
- Frequent small deliveries (lower upfront cost, no bulk discounts)
- Large, less frequent deliveries (higher initial cost, bulk purchase discounts)

### Quantity Discounts
| Purchase Quantity (liters) | Discount per Liter (CAD) |
|----------------------------|--------------------------|
| 0 - 15,000                | 0                        |
| 15,000 - 25,000           | 0.02                     |
| 25,000 - 40,000           | 0.03                     |
| 40,000+                   | 0.04                     |

---

## Business Questions

The project aims to optimize fuel inventory management by addressing:

### 1. Evaluating Current Inventory Management Practices
- **Data Preprocessing**:
  - Merge `Tanks.csv`, `Locations.csv`, and `Invoices.csv`
  - Concatenate `Fuel_Level_Part_1.csv` and `Fuel_Level_Part_2.csv`
  - Handle missing values and clean data
- **Visualization**: Assess fuel levels over time for each tank
- **Performance Analysis**: Evaluate purchase patterns and cost savings for stations 1–8

### 2. Recommending Improved Ordering Strategies
- **Maximize Discount Savings**:
  - Analyze tank capacity to determine highest applicable discount rate
  - Calculate 7-day inventory threshold for each station
  - Optimize order quantities to balance cost and inventory needs
- **Recommendations**:
  - Propose ordering strategies per location with estimated cost savings

### 3. Identifying the Best Day for Fuel Orders
- **Analyze price trends by day of the week**
- **Identify the cheapest day to purchase fuel**
- **Estimate additional savings from strategic order timing**

### 4. Evaluating Feasibility of Adding Tanks
- **Assess potential benefits of increasing tank capacity**
- **Estimate cost-benefit over a 5-year period considering inflation**
- **Identify stations where additional tanks would be most beneficial**

---

## Group Report Requirements
Teams must submit:
- A Python notebook (`.ipynb`) containing:
  - **Code**: Well-documented with meaningful comments
  - **Data Processing**: Cleaning, merging, and preprocessing steps
  - **Analysis & Visualizations**: Insights derived from data
  - **Business Questions Addressed**: Detailed responses
  - **Report Quality**: Clear structure and logical reasoning
- **Evaluation Criteria**:
  - Code clarity and logical soundness
  - Use of professional visualizations
  - Academic integrity (original work, proper citations)

The analysis will be validated by running the submitted code.

---

**Note**: Delivery costs are not considered in this project.
