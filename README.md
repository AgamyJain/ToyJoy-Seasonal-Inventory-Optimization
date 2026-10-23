# ToyJoy Seasonal Inventory Management & Optimization

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black" alt="Power BI">
  <img src="https://img.shields.io/badge/Analytics-Inventory%20Optimization-4472C4" alt="Inventory Analytics">
  <img src="https://img.shields.io/badge/Status-Completed-green" alt="Completed">
</p>

<p align="center">
  <strong>A Power BI inventory analytics project examining product demand, inventory turnover, excess inventory, stockouts, and seasonal sales patterns.</strong>
</p>

---

## Table of Contents

- [Project Abstract](#project-abstract)
- [Business Scenario](#business-scenario)
- [Business Objectives](#business-objectives)
- [Business Questions](#business-questions)
- [Dataset Overview](#dataset-overview)
- [Tools and Techniques](#tools-and-techniques)
- [Methodology](#methodology)
- [Dashboard Preview](#dashboard-preview)
- [Key Findings](#key-findings)
- [Business Recommendations](#business-recommendations)
- [Project Structure](#project-structure)
- [How to Review the Project](#how-to-review-the-project)
- [Limitations](#limitations)
- [Author](#author)

---

## Project Abstract

ToyJoy is a seasonal inventory management case study examining inventory efficiency, product demand, stockout frequency, and seasonal sales patterns. The project uses Power BI to analyze three years of historical data covering April 2023 to March 2026.

The analysis compares products using units sold, revenue, inventory turnover, stockouts, and excess inventory value. It highlights products with substantial excess inventory value, including Monopoly Classic and Robo Defender, while identifying products with comparatively high sales and recurring stockout events.

Seasonal analysis shows that the Festive Season recorded the highest demand among the six business seasons examined. Recommendations focus on reviewing excess stock, adjusting replenishment decisions according to product-level evidence, and planning inventory around seasonal demand patterns.

The project provides descriptive historical analysis rather than a validated statistical demand-forecasting model.

## Business Scenario

ToyJoy is presented as a toy retailer selling through physical stores and online channels. Management has identified a combination of excess stock and stockouts and wants to improve inventory planning, warehouse utilization, and working capital efficiency.

## Business Objectives

- Identify products with substantial excess inventory value.
- Examine product demand and inventory turnover.
- Identify products with recurring stockout events.
- Investigate seasonal differences in sales.
- Recommend product-specific replenishment and inventory management actions.

## Business Questions

1. Which products have the highest excess inventory value?
2. Which products experience recurring stockout events?
3. How does demand vary across business seasons?
4. Which products merit inventory or replenishment adjustments?
5. How can reorder planning be improved using the available historical evidence?

## Dataset Overview

| Attribute | Description |
|---|---|
| Dataset | `toyjoy_inventory.csv` |
| Source format | CSV |
| Analysis period | April 2023 – March 2026 |
| Original dataset size | Approximately 5,500 records |
| Cleaned analysis dataset | 5,330 records, as documented in the project |
| Analysis tool | Microsoft Power BI |
| Product categories | Action Figures, Dolls, Board Games, Puzzles |

The project uses a toy inventory dataset containing product, store, sales, inventory, and seasonal information. Refer to the report for the data-cleaning steps and assumptions.

## Tools and Techniques

- Microsoft Power BI
- Data cleaning and transformation
- Power Query
- DAX measures
- Inventory turnover analysis
- Product-level inventory comparisons
- Seasonal trend analysis
- Stockout analysis
- Dashboard visualization

## Methodology

### 1. Data Preparation

Inspect the source dataset, trim text fields, standardize category labels, remove duplicate product-store-date records according to the documented approach, and handle missing inventory values.

### 2. Inventory KPI Analysis

Evaluate units sold, inventory turnover, stockout frequency, revenue, and excess inventory value.

**Inventory turnover formula:**

`Inventory Turnover = Units Sold / Average Inventory`

This definition follows the project's selected measure. It should not be interpreted as a standard cost-of-goods-sold turnover ratio without considering the measure's units and assumptions.

### 3. Overstock Analysis

Compare excess inventory value across products to identify where inventory investment warrants closer review.

### 4. Stockout Analysis

Compare stockout counts and turnover across products to identify items that may need closer replenishment monitoring.

### 5. Seasonal Analysis

Compare units sold across the six business seasons represented in the dataset.

### 6. Recommendations

Develop product-specific inventory and replenishment recommendations using the observed demand, turnover, stockout, and inventory measures.

## Dashboard Preview

![ToyJoy Inventory Performance Dashboard](images/ToyJoy_Inventory_Performance_Dashboard.png)

[Open the dashboard PDF](dashboard/ToyJoy_Inventory_Dashboard.pdf)

## Key Findings

### Excess Inventory

The analysis identifies the following products as having the largest excess inventory values:

| Product | Excess Inventory Value |
|---|---:|
| Monopoly Classic | ₹37.43M |
| Robo Defender | ₹29.91M |
| Baby Doll Deluxe | ₹24.33M |

These products warrant closer review of stock levels, demand, and replenishment decisions.

### Stockout Events

Princess Doll recorded five stockout events, while Baby Doll Deluxe and SuperHero Warrior each recorded two stockout events in the documented analysis.

These observations support closer monitoring of replenishment performance for the affected products.

### Seasonal Demand

The Festive Season recorded the highest demand at approximately 19,537 units, followed by Summer Vacation at approximately 11,562 units and Regular Season at approximately 11,150 units.

These historical patterns can inform seasonal planning, but they do not by themselves constitute a validated demand forecast.

## Business Recommendations

- Review excess inventory in Monopoly Classic and Robo Defender before placing additional orders.
- Monitor Princess Doll, Baby Doll Deluxe, and SuperHero Warrior for recurring stockout events.
- Align seasonal inventory planning with the observed historical demand pattern.
- Review reorder quantities for slower-moving products using demand and inventory evidence.
- Validate proposed changes against supplier lead times, safety-stock requirements, and actual replenishment constraints.

## Project Structure

```text
ToyJoy-Seasonal-Inventory-Optimization/
├── README.md
├── data/
│   └── toyjoy_inventory.csv
├── dashboard/
│   ├── ToyJoy_Inventory_Dashboard.pbix
│   └── ToyJoy_Inventory_Dashboard.pdf
├── report/
│   └── ToyJoy_Inventory_Optimization_Report.docx
└── presentation/
    ├── ToyJoy_Executive_Presentation.pptx
    └── ToyJoy_Executive_Presentation.pdf
