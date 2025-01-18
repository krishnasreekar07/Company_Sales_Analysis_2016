# Company_Sales_Analysis_2016
# Company Sales Analysis - Power BI Project

## Project Overview
This Power BI project analyzes sales data and web events for various companies using multiple datasets. The goal of this project is to provide insights into sales performance, spending patterns, and top-performing sales representatives. The project also highlights trends in purchases made by Ford Motor Company in 2016.

---

## Datasets Used
The project uses the following CSV datasets:
1. **Accounts**: Contains information about company accounts.
2. **Sales Reps**: Includes details of sales representatives and their regions.
3. **Orders**: Contains transaction data, including total sales amounts and types of paper.
4. **Web Events**: Includes web engagement details for different companies.
5. **Regions**: Lists regions where the companies operate.

---

## Data Modeling and Relationships
The data was imported into Power BI, and relationships were established as per the provided **Entity Relationship Diagram (ERD)**:
- **Accounts ↔ Orders**: `accounts.id = orders.account_id`
- **Orders ↔ Regions**: `orders.region_id = regions.id`
- **Accounts ↔ Web Events**: `accounts.id = web_events.account_id`
- **Sales Reps ↔ Regions**: `sales_reps.region_id = regions.id`

Data modeling ensured proper connectivity between datasets for seamless analysis and reporting.

---

## Key Pages and Visualizations
### 1. **Comparison**
   - **Visualization**: Clustered Column Chart
   - **Insights**: Displays the total amount spent on standard, gloss, and poster paper, along with the total amount per region.
   - **Key Finding**: The region that spent the least amount on posters in 2016 is filtered using a slicer.

---

### 2. **Channels**
   - **Steps**:
     - Combined the `Accounts`, `Web Events`, and `Sales Reps` tables using inner joins in Power Query.
     - Grouped data by sales representative name and channel name, calculating the number of events for each.
   - **Visualization**: Column Chart
   - **Key Finding**: Identified the sales representative who engaged in the most events through the direct channel using slicers.

---

### 3. **Top Performers**
   - **Visualization**: Table Visual
   - **Insights**:
     - Highlighted sales representatives with total sales exceeding $750,000.
     - Displayed total sales, total transactions, and their respective regions.
   - **Key Finding**: Conditional formatting was applied to identify top performers, and the region with the highest number of top-performing sales representatives was highlighted.

---

### 4. **Ford_Motor_2016**
   - **Visualization**: Line Chart
   - **Insights**:
     - Analyzed Ford Motor Company’s spending trends on all paper types in 2016.
     - The date column (`occurred_at`) was converted to the `yyyy-mm-dd` format and used as a hierarchy to drill down to the month level.
   - **Key Finding**: Ford Motor Company's paper purchases in 2016 exhibited a **decreasing trend**.

---

## How to Use the Power BI File
1. **Download the File**: Clone the repository or download the `Company_Sales_Analysis_2016.pbix` file.
2. **Open in Power BI Desktop**: Use Power BI Desktop to explore the visualizations and perform additional analyses.
3. **Data Exploration**: Interact with slicers and filters to view insights tailored to specific conditions or requirements.

---

## Repository Structure
