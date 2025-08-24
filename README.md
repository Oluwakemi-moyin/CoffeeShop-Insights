# CoffeeShop-Insights
## An analysis into the sales and customer patronage level for The Daily Grind Coffee shop from Years 2019 to 2022

## Tool used: Microsoft excel for analysis.
## Introduction:
### Objective
- Find trends of total sales for each coffee type
- Generate a table or chart highlighting the top 10 customers based on their contribution to total sales.
- Find the total sales by each country
-	Find the total quantity ordered for each coffee type.
### About the data 
-	Orders table has 5 real columns and 11 empty columns. The table contains information on orders. 
-	Customers table has 9columns with incomplete rows in the email and phone number columns. The table contains information about customers. 
iii.	Products table has 7columns. The table contains information about the product (coffee, the types the coffee shop sells, unit price, roast types, price per 100g and profit). 
iv.	Sheet1 table has 2 columns. The table contains the 4 coffee types the shop sells and the fifth in the list is Sugar. 
v.	The store presently has 1,000 customers in 3countries.
## Data Analysis Steps:
i.	Deleted the 11 extra empty columns in order table
ii.	Checked for duplicates: (there was none)
iii. Changed data types(date column to datetime, size and quantity to number, profit and prices to currency)
iv.	Renamed sheets 1 table to Coffee type table
v.	Loaded each table to power query and added the tables to the data model
vi.	Renamed the tables in power query(table2 to CustomersData, etc)
vii. Added Year column to Order table using formula:
    =YEAR([@[Order Date]])
viii.	Created relationships: orders table to customers table(using customer ID), orders table to products table(using Product ID) and products table to coffee type table (renamed the sheets1 table to coffee type)(used coffee type - type)
ix.	Created total sales calculated measure in the data model using formula: 
    Total Sales:=SUMX(OrderData,OrderData[Quantity/pack]* RELATED(ProductsData[Unit Price]))
x.	Created separate sheets for the analysis. Country sales, Coffee type quantity, Top 10 customers, Sales Trends and Dashboard.
xi.	Created my dashboard and added slicers: Roast type, Date, Loyalty card and Size

## Key Findings/Insights: 
### Sales trend by Coffee type
i.	From the analysis; Excelsa coffee and Liberica coffee are the top-selling coffee types by total sales, with Arabica and Robusta following close behind. This suggests these varieties are the most profitable and popular.
ii.	Excelsa has total sales of $12,306.44 followed by Liberica with total sales of $12,054.08. Robusta has the lowest total sales of $9,005.25. 
iii. When the Coffee shop started selling in Year 2019, sales were initially fair, but reduced further in 2020 by $69.72. Sales rose in the following year 2021 to $13,766.11 which was about 13.60% increase as compared to the previous         year. However in 2022, Total Sales dropped to $7,063.44 which is a 48.68% decrease from the previous year.
iv.	In 2019, Excelsa coffee had the highest Total sales of $3,481.46 and Robusta with the lowest sales of $2,401.07. In 2020, Excelsa coffee still maintained the status quo of highest total sales with a value of $3,663.41 and Robusta        also had the lowest total sales of $2,493.27.  In 2021, Arabica coffee brought in the highest total sales of $4,045.63 and Robusta still brought in the lowest total sales. Sales was incredibly low in 2022 with Liberica taking the        lead with the highest total sales of $2,234.92 while Arabica had the lowest total sales.

### Total Sales by Country
i.	The coffee shop operates in 3 countries: The United States, The United Kingdom and Ireland.
ii.	Sales are overwhelmingly concentrated in the United States, which accounts for a substantial majority of the revenue. The United Kingdom and Ireland represent smaller but still significant markets.
iii.	United States has the highest overall sales of $35,638.89 compared to other countries. United Kingdom has the lowest overall sales of $2,798.51.
iv.	All the Coffee types have a general high total sales in The United States as compared to other countries.

### Top 10 Customers
i.	The shop has a total of 1,000 customers. However only 913 are active with orders with a total of 3,551 orders. 87 customers have not placed any orders since 2019. 
ii.	Allis Wilmore, Brenn Dundredge, Terri Farra, Nealson Cuttler, Don Flintiff, Derick Snow, Brice Romera, Alexa Sizey, Ailey Brash, Daniel Heinonen with 5 other customers vying for the 10th position. Allis has the highest overall total sales of $317.07 followed by Brenn with $307.05 with a contribution percentage of 0.70% and 0.68%. 
iii.	The top 10 customers have a total sales contribution percentage of 5.76% from the overall total sales of $45,134.26.
iv.	This shows the significant impact a few key customers can have on overall revenue. Targeting these individuals with exclusive offers could build loyalty and increase sales further.
v.	The following customers have been consistent over the years and placed orders for atleast 2years consistently: Allis Wilmore, Brenn Dundredge DuTerri Farra, Nealson Cuttler, Don Flintiff, Derick Snow, Odelia Skerme, Marja Urion and     Flynn Antony.

### Total Quantity Ordered by Coffee type
i.	While Excelsa and Liberica lead in total sales, the analysis shows that Arabica and Robusta are the most frequently ordered types by quantity. Liberica has the least frequent order.
ii.	Arabica has the highest sales quantity of 947packs followed by Robusta with 878packs. This is a critical insight for inventory management, as these two types require higher stock levels to meet demand.
iii.	This shows that although Arabica and Robusta have the highest orders, they are cheaper in price as compared to Excelsa coffee and Liberica coffee.
iv.	In terms of average price, Liberica coffee and Excelsa have the highest average prices of $15.1725 and $14.2625 respectively. This further explains why the coffee types both have higher total sales as compared to Arabica and Robusta     coffee types.
v.	No price and no quantity ordered for Sugar which could mean sugar is sold for free and not included in the orders.

### Monthly sales trend
i.	The months of June, March, April, and February have the highest sales values of $4,843.04, $4,795.78, $4,224.60 and $4,138.21 respectively.
ii.	August has the lowest overall sales of $2,326.90.

## Recommendations: 
Based on the data, these are my suggestions for the business.
i.	Marketing Strategy: Launch targeted promotions for Excelsa and Liberica to further boost their high-value sales.
ii.	Inventory Management: Ensure ample stock of Arabica and Robusta to meet consistent demand.
iii.	Customer Loyalty: Create a special program or discount for your top-contributing customers to foster brand loyalty. 
iv.	Also make inquiry from the non-active customers to know what is stopping their orders and explore ways of improving their orders e.g free/reduced delivery fee for first order.
v.	Geographical Expansion: Explore targeted marketing campaigns in the UK and Ireland to grow these smaller markets. 
