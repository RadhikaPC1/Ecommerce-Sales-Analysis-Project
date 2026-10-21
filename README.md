# E-commerce Sales Analysis Dashboard (Power BI)

An interactive Power BI dashboard that tracks e-commerce sales performance across product categories, markets, countries, states, and shipping modes. It gives a business team a single-page view of **Sales, Profit, Quantity, and Shipping Cost**, with slicers to drill into any category or market.


---

## Business Problem

An e-commerce business needs quick answers to recurring questions:

- Which product categories drive the most sales?
- Which markets, countries, and states contribute the most revenue?
- Which shipping modes do customers use most, and what does shipping cost the business?
- How healthy is profitability relative to sales and shipping spend?

This dashboard replaces manual reporting with one interactive view that answers these questions in seconds.

---

## Dataset

| Item | Detail |
|------|--------|
| File | `ECOMM_DATA.xlsx` (Global Superstore-style e-commerce sample dataset) |
| Source link | [Add link if downloaded from Kaggle or another site] |
| Sheets | `Orders`, `Returns`, `People` |
| Records | **51,290** order-line rows, 24 columns |
| Period | **January 2011 to December 2014** (order dates) |
| Unique Orders | 25,035 |
| Unique Customers | 1,590 |
| Unique Products | 10,292 |
| Coverage | 7 markets, 147 countries, 1,094 states |
| Customer Segments | Consumer, Corporate, Home Office |
| Product Hierarchy | 3 categories, 17 sub-categories |

**Fields in `Orders`:** Row ID, Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Customer Name, Segment, City, State, Country, Postal Code, Market, Region, Product ID, Category, Sub-Category, Product Name, Sales, Quantity, Discount, Shipping Cost, Profit, Order Priority

**Fields used in the dashboard:** Category, Market, Country, State, Ship Mode, Sales, Quantity, Profit, Shipping Cost

**Totals:** Sales $12.64M | Profit $1.47M | Quantity 178,312 | Shipping Cost $1.35M

---

## Headline KPIs

| KPI | Value |
|-----|-------|
| Sales | **$12.64M** |
| Profit | **$1.47M** |
| Quantity Sold | **178K units** |
| Shipping Cost | **$1.35M** |
| Profit Margin (Profit ÷ Sales) | **~11.6%** |
| Shipping Cost as % of Sales | **~10.7%** |
| Average Sales per Unit | **~$71** |

---

## Dashboard Visuals

| Visual | Purpose |
|--------|---------|
| KPI cards (Sales, Profit, Quantity, Shipping Cost) | Headline performance at a glance |
| Column chart: Sales by Category | Compare category performance |
| Pie chart: Sales by Market | Show each market's share of sales |
| Funnel chart: Sales by Ship Mode | Compare sales across shipping modes |
| Donut chart: Top 7 Sales by Country | Identify the highest-selling countries |
| Column chart: Top 5 Sales by State | Identify the highest-selling states |
| Filled map: Sales by Country | Geographic view of sales distribution |
| Slicers: Category, Market | Filter the whole dashboard interactively |

---

## Key Insights

**1. Profitability is healthy but thin.**
Sales of $12.64M generated $1.47M in profit, an overall margin of about **11.6%**, or roughly $8 of profit per unit sold across 178K units.

**2. Shipping cost nearly equals total profit.**
Shipping cost is $1.35M, about **10.7% of sales** and roughly **92% of the profit earned**. Shipping is the biggest controllable cost visible in the dashboard: a 10% cut in shipping cost (~$0.14M) would lift profit by about 9%.

**3. Technology is the top category, but categories are close.**
Technology leads with **$4.7M (~37%)**, followed by Furniture at **$4.1M (~32%)** and Office Supplies at **$3.8M (~30%)**. Sales are fairly balanced, with only a ~$0.9M gap between first and last, so the business is not dependent on a single category.

**4. APAC and EU drive over half of sales.**
APAC leads with **$3.59M (28.4%)**, followed by EU at **$2.94M (23.2%)**, together about **52%** of total sales. Adding US ($2.30M, 18.2%) and LATAM ($2.16M, 17.1%), the top four markets account for roughly **87%** of sales. Canada is the smallest market at just **0.5%** ($0.07M).

**5. The United States is the single largest country.**
The US contributes **$2.30M**, ahead of Australia ($0.93M), France ($0.86M), China ($0.70M), and Germany ($0.63M). The top 7 countries together make up about **$6.6M, roughly half (~52%) of all sales**.

**6. Sales are spread across many states, not concentrated.**
The top 5 states, led by **England ($0.49M)** and **California ($0.46M)** followed by Ile-de-France ($0.32M), add up to only about **$1.85M (~15% of sales)**. Revenue comes from a broad geographic base rather than a few hotspots.

**7. Standard Class dominates shipping.**
Standard Class accounts for roughly **$7.6M (~60%)** of sales, followed by Second Class ($2.57M, ~20%), First Class ($1.83M, ~14%), and Same Day ($0.67M, ~5%). Customers strongly prefer the cheapest, slowest option, and premium speed is a small share of revenue.

---

## Recommendations

1. **Review shipping cost per order.** Since shipping cost is almost as large as profit, renegotiate carrier rates, review free-shipping thresholds, and optimize fulfillment by region.
2. **Protect and grow APAC and EU.** They are the two largest markets, so prioritize inventory, marketing, and delivery performance there.
3. **Evaluate small markets.** Canada (0.5%) and the smaller EMEA and Africa markets contribute little. Decide whether to invest to grow them or reduce cost-to-serve.
4. **Balance category strategy.** Keep investing in Technology as the top seller, and look for margin improvement in Furniture and Office Supplies.
5. **Promote faster shipping selectively.** Same Day is only ~5% of sales. Test whether paid express shipping can lift revenue without raising shipping cost.

---

## Tools Used

- **Power BI Desktop:** data modeling, visuals, slicers, and report design
- **DAX / Aggregations:** Sum of Sales, Quantity, Profit, and Shipping Cost
- **Top N filtering:** Top 7 countries and Top 5 states

---

## How to Use

1. Clone or download this repository.
2. Open `Ecommerce_Sales_Analysis.pbix` in **Power BI Desktop**.
3. Use the **Category** and **Market** slicers to filter the dashboard.
4. Click any chart element to cross-filter the other visuals.

---

## Limitations and Future Improvements

- Add profit and margin by category, market, and country to show where profit is actually made, not just sales.
- Add month-over-month and year-over-year trend analysis.
- Add AOV and return rate measures.
- Add a sales forecast with forecast vs. actual comparison.
- Add SQL scripts for data extraction and KPI validation.

---
