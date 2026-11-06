# Supply Chain & Operational Performance Analysis using Power BI

## Project Overview

An interactive Power BI dashboard analysing order trends, delivery performance, carrier efficiency and revenue using a synthetic supply chain dataset from DSE Africa / Data East Africa.

## Tools & Technologies

- Power BI
- Power Query
- DAX

## Data Preparation

- Imported and cleaned six datasets: logistics_orders, logistics_order_items, logistics_reviews, logistics_carriers, logistics_sellers, logistics_customers.
- Checked duplicates, missing values and data types.
- Created a binary "valid_delivery_flag" (1 = valid, 0 = invalid) in Power Query to identify reliable delivery records. Valid records required a delivered status, non-missing dispatch and delivery dates, and a delivery date on or after the dispatch date. This helped ensure that OTD calculations used only valid delivery records.
- Established relationships between orders, order items, reviews, carriers, sellers, customers.

## DAX & Measures

Created DAX measures to calculate dashboard KPIs and additional metrics, including:

- Average Delivery Time (Days)
- Average Order Value
- Cancelled Orders
- Category Order Count
- Delayed Orders
- Review Rating

## Key Performance Indicators

- Total Orders
- Delivered Orders
- On-Time Delivery (OTD %)
- Delayed Orders
- Average Delivery Time
- Delivered Item Revenue

## Dashboard Analysis

- Monthly order volume and on-time delivery trends.
- Order fulfilment funnel.
- Delivered item revenue by product category.
- Carrier delivery performance.
- On-time delivery performance by service type.
- Review rating distribution.

Key Insights

1. Order Volume & Delivery Performance: Order volume increased by approximately 29% from November to December 2023 (1,546 to 1,995), while OTD declined from 71.8% to 58.7%. OTD recovered to 85.5% in January 2024.

2. Carrier & Service Type Performance: Tembo Freight exclusively handled National Road Courier (Economy) shipments in the dataset, accounting for 5,211 valid deliveries with an OTD of 56.0%—substantially below the 83.2%–88.6% range recorded by the other carriers and service types.

## Project Files

- [Power BI Dashboard (.pbix)](./Supply%20Chain%20%26%20Delivery%20Performance%20Dashboard.pbix)
- [Dashboard PDF (.pdf)](./Supply%20Chain%20%26%20Delivery%20Performance%20Dashboard.pdf)

## Dataset & Limitations

The project uses a synthetic educational dataset from DSE Africa / Data East Africa. Review score criteria are undocumented, so ratings are presented as a neutral distribution rather than a specific measure of delivery or product satisfaction.

OTD is calculated as on-time valid deliveries divided by total valid deliveries. Orders with missing or invalid delivery dates are excluded from this calculation.

The valid delivery count is slightly lower than the delivered order count because some orders marked as delivered had missing or invalid delivery dates. Delivery performance calculations, including OTD, are based on valid deliveries rather than all delivered orders.

---

*Built by Gargi Barman*
