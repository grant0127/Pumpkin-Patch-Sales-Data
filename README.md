# Church Fundraiser Sales Analysis: Power BI Dashboard

## Overview

This project uses a Power BI dashboard to analyze sales from a church fundraiser and identify how to grow profit at next year's events. The dashboard breaks profit down by **day of the week**, **hour of the day**, and **product size (circumference)**, with slicers for filtering by day and size.

**Total profit in the dataset: $47,067**

![Dashboard](dashboard.png)

## Tools Used

- Power BI
- DAX
- Excel

## Dataset

## Dataset

This dataset contains pumpkin sales transactions from a church pumpkin patch fundraiser. Each row is one line item in a transaction, recording when the sale happened, which size of pumpkin was sold, how many were sold, and the cost, price, and profit.

2281 rows of data, sourced directly from church, all sales were from October 1st to 31st.

| Column | Description |
|---|---|
| `Transaction ID` | Unique identifier for each transaction |
| `Sale Date` | Date the sale took place |
| `Day of Week` | Day of the week the sale took place (Monday to Sunday) |
| `Sale Time` | Time of day the sale took place, used to build the hourly profit view |
| `Transaction Total Pumpkins` | Number of pumpkins sold in the transaction (summed as quantity in the dashboard) |
| `Pumpkin Circumference` | Size of the pumpkin sold, measured by circumference *(add the unit, e.g. inches)* |
| `Unit Cost` | What the pumpkin cost the church per unit |
| `Unit Price` | What the customer paid per unit |
| `Line Profit` | Profit on the line item, calculated as (unit price − unit cost) × quantity |

### Data Preparation

The original dataset did not include profit nor a way to present the time for the sales, a column was created to display sale time neatly.

## Key Findings

- **Weekends drive profit.** Saturday and Sunday together account for about $17.6K of the $47K total.
- **Profit is concentrated in the late afternoon.** The 4 PM and 5 PM hours together contribute $23K, close to half of total profit.
- **Early-day hours and early-week days are underperforming.** Both are volume gaps, which makes them good targets for promotions.
- **Mid-range sizes perform best.** Sizes 24 to 31 account for the largest share of profit.

## Recommendations

### 1. Run a Buy One Get One 50% Off deal on Monday, Tuesday, and Wednesday
Monday to Wednesday are the three lowest-profit days (Monday $4.9K, Tuesday $4.4K, Wednesday $5.5K), and the data shows the gap comes from lower volume. A BOGO 50% deal gives customers a reason to order on slower days and to buy more per order.

### 2. Offer 25% off the total order from 11 AM to 2 PM
The earliest hours are the weakest on the dashboard (11 AM at $1.3K, 12 PM at $3.1K, 1 PM at $4.1K). A midday discount aims to pull demand forward into hours that are currently underused.

### 3. Release a discount code on social media to grow the church's following
Share a promo code on the church's social media platforms so customers follow the church and stay in the loop for future fundraisers and events. This builds an audience that can be reached directly the next time the church runs a sale or event.

### Discount rules
- **Discounts do not stack.** Each order can use only one offer (BOGO, the midday discount, or the social media code).
- The offers target different gaps in the data (slow days, slow hours, and audience growth), so they work as a set without needing to overlap.

### How to measure success
- Quantity and profit on Monday to Wednesday compared with this year's baseline
- Profit during the 11 AM to 2 PM window compared with this year's baseline
- Social media code redemptions and new followers gained
- Profit per order, to make sure the discounts add enough volume to offset the lower margin

```
