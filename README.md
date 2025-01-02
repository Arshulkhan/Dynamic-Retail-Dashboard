# Dynamic-Retail-Dashboard
### Dynamic Retail Dashboard Overview

The Dynamic Retail Dashboard is an advanced Excel-based solution designed to provide visualization and analysis of retail data. Leveraging Power Query for data transformation and integrating with datasets hosted on GitHub, the dashboard delivers actionable insights through dynamic charts and Key Performance Indicators (KPIs). This tool addresses crucial retail business challenges, enabling data-driven decision-making.

---

### Key Datasets Used

**1. Orders Table**  
This table provides comprehensive details about customer orders, including product, shipping, and financial metrics.  
*Sample Data:*

| Order ID       | Returned | Order Date | Ship Date | Ship Mode      | Customer Name | Segment     | Country       | Market | Sales   | Profit  | Discount |
|----------------|----------|------------|-----------|----------------|---------------|-------------|---------------|--------|---------|---------|----------|
| CA-2012-124891 | No       | 31-07-2020 | 31-07-2020 | Same Day       | Rick Hansen   | Consumer    | United States | US     | 2309.65 | 762.18  | 0        |
| IN-2013-77878  | Yes      | 05-02-2021 | 07-02-2021 | Second Class   | Justin Ritter | Corporate   | Australia     | APAC   | 3709.40 | -288.77 | 0.1      |
| IN-2013-71249  | No       | 17-10-2021 | 18-10-2021 | First Class    | Craig Reiter  | Consumer    | Australia     | APAC   | 5175.17 | 919.97  | 0.1      |

**2. Returns Table**  
This table tracks returned orders along with their respective markets.  
*Sample Data:*

| Returned | Order ID       | Market  |
|----------|----------------|---------|
| Yes      | MX-2013-168137 | LATAM   |
| Yes      | US-2011-165316 | LATAM   |
| Yes      | ES-2013-1525878| EU      |
| Yes      | CA-2013-118311 | US      |

**3. People Table**  
This table provides information about sales representatives and their regional coverage.  
*Sample Data:*

| Person           | Region   |
|------------------|----------|
| Anna Andreadi    | Central  |
| Chuck Magee      | South    |
| Kelly Williams   | East     |
| Matt Collister   | West     |
| Deborah Brumfield| Africa   |

---

### Addressed Problem Statements and Steps

#### 1. Key Performance Indicators (KPIs)
**Objective:** Dynamically display metrics like Total Sales, Profit, Quantity, Order Count, and Profit Margin.

**Steps:**
1. Import the Orders Table into Power Query for processing.
2. Create calculated columns:
   - **Profit Margin**: `Profit / Sales`
   - **Total Orders**: Count of `Order ID`
3. Use Excel formulas to compute:
   - **Total Sales**: `=SUM(Sales)`
   - **Total Profit**: `=SUM(Profit)`
   - **Total Quantity**: `=SUM(Quantity)`
4. Create a dynamic KPI table with visual enhancements (e.g., symbols like “💰” for Total Sales).

| Metric           | Calculation          | Symbol |
|------------------|----------------------|--------|
| Total Sales      | Sum of Sales         | “💰” |
| Total Profit     | Sum of Profit        | “📈” |
| Total Quantity   | Sum of Quantity      | “📦” |
| No. of Orders    | Count of Order IDs   | “🛒” |
| Profit Margin    | Sum of Profitability | “🔹” |

#### 2. Sales and Profit Analysis
**Objective:** Visualize sales and profit trends.

**Steps:**
1. Create a Pivot Table grouping `Order Date` by Year and Month.
2. Add `Sales` and `Profit` as values.
3. Design a Line Chart for trend visualization.
4. Integrate Slicers for dynamic filtering by category, market, or region.

![image](https://github.com/user-attachments/assets/9d35423f-76da-437b-bd2c-311675c4dacf)


#### 3. Category-Wise Profit
**Objective:** Evaluate profit across product categories.

**Steps:**
1. Create a Pivot Table with `Category` as rows and `Profit` as values.
2. Sort data by descending `Profit`.
3. Develop a Bar Chart to display category-wise profit.
4. Add Slicers for year and region-based filtering.

#### 4. Segment-Wise Sales Share (%)
**Objective:** Visualize sales share by customer segment.

**Steps:**
1. Build a Pivot Table with `Segment` as rows and `Sales` as values.
2. Compute percentage share: `Sales / Total Sales * 100`.
3. Create a Pie or Donut Chart for visual representation.
4. Include labels for percentage values.

#### 5. Sales by Country
**Objective:** Analyze sales performance by country.

**Steps:**
1. Develop a Pivot Table with `Country` as rows and `Sales` as values.
2. Sort data in descending order of `Sales`.
3. Apply Conditional Formatting or Heatmaps to highlight top-performing countries.
4. Optionally, use a Geographic Map Chart for a global view.

#### 6. Top 5 Subcategories
**Objective:** Identify top-performing subcategories.

**Steps:**
1. Build a Pivot Table with `Sub-Category` as rows and `Sales` as values.
2. Sort by descending `Sales` and filter to show Top 5 Subcategories.
3. Design a Column Chart for visualization.

#### 7. Bottom 5 Subcategories
**Objective:** Highlight underperforming subcategories.

**Steps:**
1. Use the same Pivot Table but sort by ascending `Sales`.
2. Filter to display Bottom 5 Subcategories.
3. Develop a Column Chart with contrasting colors for emphasis.

#### 8. Yearly Sales Trends
**Objective:** Track yearly sales trends.

**Steps:**
1. Group `Order Date` by Year in a Pivot Table.
2. Add `Sales` as a value.
3. Create a Line Chart to illustrate trends.
4. Enable Slicers for filtering by category, region, or segment.

---

### Dynamic Features
- **Dynamic Charts:** Update automatically based on slicer selections.
- **Power Query Integration:** Streamlines data cleaning and transformation.
- **Interactive KPIs:** Provide instant insights into key metrics.

---

### Future Enhancements

**Potential Extensions:**
- **Return Analysis:** Investigate return rates by market and category.
- **Customer Insights:** Identify most and least profitable customers.
- **Market Performance:** Compare performance across different markets.
- **Product Evaluation:** Assess individual product profitability.

---

### Business Significance

The Dynamic Retail Dashboard empowers businesses to:
- Monitor vital metrics through KPIs.
- Discover trends across categories, segments, and geographies.
- Make informed strategic decisions to enhance performance.

**Visual Representations:**
The accompanying GitHub repository contains visuals for all problem solutions, including screenshots of the complete dashboard in action.

