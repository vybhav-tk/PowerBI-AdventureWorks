![image](https://github.com/user-attachments/assets/dfb7a672-2775-496e-bcc8-a2415eb87dd1)

![image](https://github.com/user-attachments/assets/76c83122-b68a-4e56-8b2d-6e14048f47f1)

![image](https://github.com/user-attachments/assets/5085e4f9-59ea-4ebe-b184-fef65c21f92f)

![image](https://github.com/user-attachments/assets/0f29c547-acb6-4d85-9931-9d0d7b16b1e4)


# AdventureWorks Power BI Dashboard

This repository contains a comprehensive Power BI dashboard built for **AdventureWorks**, a fictional global retailer. The dashboard provides a deep analytical view of sales, products, customer behavior, and executive-level performance metrics. It is designed to empower business stakeholders with data-driven insights through intuitive visualizations and powerful interactivity.

The project incorporates advanced Power BI features such as custom tooltips, drillthrough, bookmarks, slicer panels, navigation buttons, and parameters, showcasing not only technical expertise but also thoughtful user experience design.

---

## Data Sources

The following datasets were used in this project:

- `Sales Data`
- `Product Lookup`
- `Customer Lookup`
- `Territory Lookup`
- `Calendar Table`
- `Return Data`

These tables include information on transactions, customer profiles, product details, regional mappings, time intelligence, and product returns.

---

## Project Overview

The project is divided into four main parts:

1. **Connecting and Shaping the Data**  
2. **Data Modeling**  
3. **Adding DAX Measures & Calculated Columns**  
4. **Building the Report**

---

## Part 1: Connecting and Shaping the Data

### Key Transformations:
- Promoted headers and confirmed data types across all tables.
- Created calculated columns including:
  - Full customer name
  - Age from birthdate
  - Regional abbreviations and classification flags
- Combined and cleaned return and sales data for integrity.
- Applied data profiling tools to detect and resolve nulls, blanks, and mismatches.

---

## Part 2: Creating the Data Model

### Schema Design:
- **Star schema** with:
  - Fact tables: `Sales`, `Returns`
  - Lookup tables: `Calendar`, `Products`, `Customers`, `Territories`
- One-to-many relationships with unidirectional filter flow from lookups to fact tables.

### Enhancements:
- Hidden keys and unused fields from report view.
- Proper data categorization for geospatial fields.
- Added time intelligence fields in the Calendar table.

---

## Part 3: Adding DAX Measures

### Metrics Developed:

#### Customer & Sales Metrics:
- `Total Orders`
- `Total Revenue`
- `Total Profit`
- `Total Returns`
- `Return Rate`

#### Time Intelligence:
- `Current Month Revenue`
- `Previous Month Revenue`
- `YTD Revenue`
- `Last 30/60 Day Rolling Revenue`
- `Revenue Targets`

#### Customer Detail Logic:
- `Top Customer Name`, `Revenue`, `Orders`
- Tie-handling with `HASONEVALUE()` and fallback logic

#### KPIs:
- Most ordered and returned product types
- Top revenue customers
- Rank-based metrics

---

## Part 4: Building the Report

The dashboard includes **four core pages** with a consistent and interactive design:

---

### Executive Dashboard

- **KPI Cards** with trends and target comparisons
- **Line Chart** with drill-up/down (Year > Month)
- **Matrix**: Top products by volume with conditional formatting
- **Bar Chart**: Orders by category
- **Dynamic KPIs**: Most ordered & returned categories
- **Custom Tooltip**: Category-level KPIs and weekly trend
- **Clear Filters Button** using a bookmark
- **Slicer Panel** (toggleable): Filter by year and continent

---

### Global Map View

- **Bubble Map** of orders by country using Bing Maps
- **Continent Slicer**: Styled as tile buttons for interactivity
- Auto-zoom and lasso selection enabled
- Optional lat/long usage for accuracy

---

### Product Detail Report

- **Drillthrough-enabled** from other pages
- **Gauge Charts**: Orders, revenue, and profit vs. targets
- **Area Charts**: Weekly profit and returns
- **Price Adjustment Slider**: Numeric parameter for what-if analysis
- **Dynamic Measures**: Adjusted price, revenue, and profit
- **Fields Parameter Slicer**: Toggle between KPIs (orders, revenue, returns, etc.)

---

### Customer Detail Report

- **Line Chart** toggling between `Total Customers` and `Revenue per Customer`
- **Top Customer Cards** with HASONEVALUE logic
- **Demographic Donut Charts** for gender and occupation
- **Data Table**: Top 100 customers
- **Report Interactions**:
  - Table and chart filtering rules customized
- **Bookmark** to showcase insight (e.g., "Top Customer in 2022")
- **Reset Filters Button** using a bookmark

---

## Navigation System

- **Custom Page Navigation** built with blank buttons and PNG icons
- Configured for all report pages
- Hover and press states for user feedback

---

## Advanced Features & UX Enhancements

- **Custom Report Page Tooltips**
- **Drillthrough Filters** on product-level visuals
- **Drill Up/Down** in hierarchy visuals (date-based)
- **Edit Interactions** for cross-filter control
- **Slicer Panel Toggle** via button with bookmarks
- **Numeric Parameters** for scenario testing
- **Fields Parameters** for dynamic Y-axis control
- **Bookmarks** for navigation, insight callouts, and state control

---

## Key Learnings & Concepts Demonstrated

- Power Query transformations and data shaping
- Data modeling with star schema
- One-to-many cardinality and filter direction
- DAX for KPIs, time intelligence, and interactivity
- UX design using bookmarks, slicer panels, navigation
- What-if analysis using parameters
- Custom tooltip creation and report storytelling

---

This Power BI project goes beyond static dashboards and explores **interactive storytelling**, **scenario planning**, and **executive-level reporting**. It emphasizes strong data modeling practices and combines technical depth with a polished user experience.

This dashboard is a blueprint for designing data experiences that deliver **value, clarity, and impact**.

---

