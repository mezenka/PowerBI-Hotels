# PowerBI
Short project using a hotel network revenue dataset for 2018-2020 to answer business questions:
(1) What is the revenue trend?
(2) How do individual hotels perform?
(3) Is it necessary to invest in increasing parking lots? 

**Step 1**
Loaded data into Microsoft SQL Server Management Studio as separate CSV files

**Step 2**
Prepared data for loading into Microsoft Power BI
SQL query:
WITH hotels AS
(
SELECT * FROM dbo.h2018
UNION
SELECT * FROM dbo.h2019
UNION
SELECT * FROM dbo.h2020
)
SELECT * FROM hotels
LEFT JOIN dbo.hmarket_segment
ON hotels.market_segment = hmarket_segment.market_segment
LEFT JOIN dbo.hmeal_cost

**Step 3**
Imported the data from Microsoft SQL Server into Microsoft Power BI and created the following interactive visuals:
- Cards for total revenue, average rates, nights booked, average discount applicable, number of parking spaces used
- Line chart describing revenues earned by individual hotels during the analyzed period
- Doughnut chart showing shares of individual hotels in the total revenue
- Matrix table describing revenue, total nights booked, revenue per night, required parking spaces and their percent in total bookings detailed by year and by individual hotel
Built in slicers for filtering the visuals by date, individual hotel, country

