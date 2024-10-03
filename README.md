# Toys Factory Regional Sales Analysis

## Project Overview

This project focuses on analyzing monthly sales data for a toy factory to evaluate regional sales performance. The analysis employs various filters and key performance indicators (KPIs) calculated using advanced Excel formulas to derive insights that guide business decisions and strategies.

## Technologies Used

- **Excel**: For data analysis and processing.

## Installation

1. Clone the repository to your local machine using:

   ```bash
   git clone https://github.com/yourusername/toy-factory-regional-sales-analysis.git
   ```

2. Open the `Maven_Toys_Monthly_Sales_Data.xlsx` file in Microsoft Excel or any compatible spreadsheet software.

## Key Metrics Calculated

- **Filters** :
- **Region Filter** : Selects the region for analysis.
- **Date Filter** :

  - Current Year: `=MAX(Data[Year])`
  - Current Month: `=MAXIFS(Data[Month], Data[Year], CurYear)`
  - Previous Year: `=CurYear - 1`
  - Previous Month: `=IF(CurMonth = 1, 12, CurMonth - 1)`
  - Previous Month Year: `=IF(CurMonth = 1, PrevYear, CurYear)`
  - Current Period: `=VLOOKUP(CurMonth, A16:B27, 2, 0) & " " & CurYear`

- **Key Performance Indicators (KPIs)** :

  - **Total Revenue** : =SUMIFS(Data[Revenue], Data[Region], Region, Data[Month], CurMonth,
    Data[Year], CurYear)
  - **Previous Year Revenue** : =SUMIFS(Data[Revenue], Data[Region], Region, Data[Month], CurMonth, Data[Year], PrevYear)
  - **Previous Month Revenue** : =SUMIFS(Data[Revenue], Data[Region], Region, Data[Month], PrevMonth, Data[Year], PMYear)
  - **Year-over-Year % Change**
  - **Month-over-Month % Change**

- **Store Performance**

  - **Month-over-Month % Change:** =INDEX($M$3:$P$12, MATCH($S3, $Q$3:$Q$12, 0), MATCH(W$2, $M$2:$P$2, 0))

- **Product Performance** :

  - Top 6 Performing Products
  - Bottom 6 Performing Products

## Advanced Excel Calculations

This analysis incorporates advanced Excel calculations including:

- Nested `IF` statements for date comparisons.
- `SUMIFS` for conditional summation based on multiple criteria.
- `VLOOKUP` for dynamic data retrieval.
- Array formulas for indexing and matching data across ranges.

## Findings

- Identified trends in regional sales performance over time.
- Evaluated the effectiveness of different product lines and regions.
- Provided actionable insights to enhance sales strategies and improve revenue.
