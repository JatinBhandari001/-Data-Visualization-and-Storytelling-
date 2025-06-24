<h1> Dataset use </h1>
The dataset used for this project is the Superstore Sales Dataset. It contains transactional records from a fictional retail store, capturing various dimensions of business operations.

It includes the following key features:

1. Order Information: Order ID, Order Date, Ship Date, Shipping Mode <br>
2. Customer Details: Customer ID, Customer Name, Segment<br>
3. Geographical Data: Country, Region, City, State, Postal Code <br>
4. Product Details: Category, Sub-Category, Product Name <br>
5. Financial Metrics: Sales, Quantity, Discount, Profit

<i> Data Source: Kaggle superstore.csv </i> 

<h3> Tools useds </h3>
-> Excell for data cleaning <br>
-> PowerBI for data visualization


<h1>Summary report</h1>

**Overall Financials**:

Sales: $349K | Profit: $32K | Profit Margin: 9.2% <br>
Orders Processed: 719 | Units Sold: 5,723

**Key Business Insights**:

Consumer Segment drives over 50% of sales. <br>
Technology category leads revenue at $133K. <br>
Profitability strongest in 2016; recent years show some fluctuation.

**Operational Challenges:**

65% Late Shipments (>3 days) indicate urgent need for logistics improvement.

**Strategic Focus Areas:**

Strengthen supply chain efficiency to reduce late deliveries. <br>
Leverage high-performing products and categories to drive sustained growth. <br>
Target Corporate and Home Office segments for diversification

<h2>Data Visualization and storytelling</h2>

<p><strong> Description :</strong>Interactive Power BI dashboard showcasing data visualization and storytelling techniques, focusing on key insights, trends, and actionable findings..</p>

![image](https://github.com/user-attachments/assets/445ef1a5-fa1c-4c71-ba87-06aae41c38c7)

New measures created:-

1. Profit margin percent= profitmargin% = sum(Superstore_raw_data[Profit])/SUM(Superstore_raw_data[Sales])*100 <br>
2. Late shipments =Late Shipments % = 
DIVIDE(
    COUNTROWS(
        FILTER(
            'Superstore_raw_data',
            'Superstore_raw_data'[Shipping delay(days)] > 3
        )
    ),
    COUNTROWS('Superstore_raw_data') 
) * 100  <br>

3. Shipment delay= Shipping delay(days) = 
DATEDIFF(
    'Superstore_raw_data'[Order Date], 
    'Superstore_raw_data'[Ship Date], 
    DAY
)


