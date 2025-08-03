# 🎧📊 Promo AirPods Sales Dashboard – Visualizing Performance with Power BI

## Problem Statement

"The client wanted to understand how the Promo AirPods campaign is performing across different regions, genders, and sub-categories — and how it compares to last year’s sales and this year's targets.

However, data was spread across multiple tables without a clear view of:

YTD progress,

Customer purchase patterns,

Profitability by product type,

Budget alignment."


### Steps followed 

Built a comprehensive Power BI dashboard connecting orders, transactions, and budget data. It now tracks:

YTD Sales vs Budget

Category/Segment behavior

Payment preferences

Profit by Product Line

I designed an end-to-end Promo AirPods Sales Dashboard in Power BI by integrating raw sales, budget, and product-level data.

✅ Unified Data Model: Combined 3 data sources (Orders, Details, Budget) with clean relationships and DAX-driven logic.

✅ YTD Sales Intelligence: Compared 2023 vs 2022 YTD figures, normalized to today’s date, to give a fair growth percentage.

✅ Budget vs Actual Tracking: Showed where actual sales stand against projected 2023 budgets, enabling proactive decision-making.

✅ Profitability by Sub-Category: Highlighted top-performing AirPods models based on net profit, helping marketing prioritize promotions.

✅ Customer Segmentation: Visualized sales breakdown by Category (Male/Female/Unisex) and Payment Mode, offering actionable insights on buyer behavior.

✅ Monthly Trend Visualization: Used an area chart to show profit drop-offs or spikes by month, ideal for aligning marketing and supply chain.

✅ UX Optimized for Leadership: Used KPIs, slicers (by gender), tooltips, and clean layout for a dashboard that enables leadership to make decisions fast — no digging required.

✅ Scalable for Future Campaigns: The model can be easily extended to other product lines or seasonal campaigns by simply updating the source files.

for creating new column following DAX expression was written;
       
🧮 1. YTD Sales 2023
dax
Copy
Edit
YTD Sales 2023 =
CALCULATE(
    SUM(Details_1[Amount]),
    FILTER(
        Orders_1,
        YEAR(Orders_1[Order Date]) = 2023 &&
        Orders_1[Order Date] <= TODAY()
    )
)
🧮 2. YTD Sales 2022
dax
Copy
Edit
YTD Sales 2022 =
CALCULATE(
    SUM(Details_1[Amount]),
    FILTER(
        Orders_1,
        YEAR(Orders_1[Order Date]) = 2022 &&
        Orders_1[Order Date] <= DATE(2022, MONTH(TODAY()), DAY(TODAY()))
    )
)
🧮 3. Growth % (2022 vs 2023)
dax
Copy
Edit
Growth 22 vs 23 =
DIVIDE(
    [YTD Sales 2023] - [YTD Sales 2022],
    [YTD Sales 2022]
)
🧮 4. Budget 2023
dax
Copy
Edit
Budget 2023 =
CALCULATE(
    SUM(Budget[Amount]),
    Budget[Year] = 2023
)
🧮 5. Profit by Sub-Category
Use in a visual:

Axis: Details_1[Sub-Category]

Values: SUM(Details_1[Profit])

Or create a measure:

dax
Copy
Edit
Total Profit =
SUM(Details_1[Profit])
🧮 6. Profit by Month
Ensure Order Date is in the axis (Month format) and plot:

SUM(Details_1[Profit])

SUM(Details_1[Amount])

Optional Measures:

dax
Copy
Edit
Monthly Profit = 
CALCULATE(
    SUM(Details_1[Profit]),
    FILTER(
        Orders_1,
        YEAR(Orders_1[Order Date]) = 2023
    )
)

Monthly Sales = 
CALCULATE(
    SUM(Details_1[Amount]),
    FILTER(
        Orders_1,
        YEAR(Orders_1[Order Date]) = 2023
    )
)
🧮 7. Payment Mode Share (for pie chart)
Use:

Legend: Details_1[PaymentMode]

Values: SUM(Details_1[Amount])

Or measure:

dax
Copy
Edit
Payment Amount = SUM(Details_1[Amount])


        thus, more customers have travel type 'Business'.
