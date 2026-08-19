# Customer Shopping Behavior Analysis 🛍️

Hey! This is a project where I dug into customer shopping data to understand *why* people buy what they buy. I looked at 3,900 purchases and tried to answer questions any retail team would actually care about — like who's spending more, which products rely on discounts, and whether subscribers are actually worth more to the business.

## What's this project about?

I wanted to go through the full journey a data analyst would: clean messy data, explore it in Python, dig into business questions with SQL, and finally build a dashboard someone non-technical could actually use. So that's exactly what I did.

## The Data

- 3,900 customer transactions
- 18 columns covering demographics (age, gender, location), purchase details (item, category, amount), and shopping behavior (discounts, subscriptions, review ratings, shipping type)
- Had 37 missing review ratings that I cleaned up along the way

## Tools I used

- **Python (Pandas)** — cleaning the data and exploring it
- **PostgreSQL** — answering business questions with SQL
- **Power BI** — building an interactive dashboard
- **Jupyter Notebook** — where it all comes together

## Cleaning things up

Before any analysis, I had to get the data into shape:
- Filled in missing review ratings using the median for each product category
- Renamed all the columns to snake_case so they're easier to work with
- Created a couple of new columns — `age_group` and `purchase_frequency_days` — to make the data more useful
- Noticed `discount_applied` and `promo_code_used` were basically saying the same thing, so I dropped the duplicate
- Pushed the clean data into PostgreSQL to run SQL queries on it

## Questions I answered with SQL

1. Who spends more — male or female customers?
2. Which customers used a discount but still spent above average?
3. What are the top 5 highest-rated products?
4. Does Express shipping actually lead to bigger purchases than Standard?
5. Do subscribers spend more than non-subscribers?
6. Which products rely most heavily on discounts to sell?
7. How do customers break down into New, Returning, and Loyal?
8. What are the top 3 products in each category?
9. Are repeat buyers more likely to subscribe?
10. Which age group brings in the most revenue?

You can check out all the queries here: [`customer_behavior_sql_queries.sql`](./customer_behavior_sql_queries.sql)

## What I found

- **Men outspend women** — total revenue from male customers was about $157.9K vs $75.2K from women
- **Some products basically only sell on discount** — hats, sneakers, and coats had discount rates near 50%
- **Non-subscribers actually bring in way more total revenue** ($170K vs $62.6K) — even though the average spend per person is pretty similar between the two groups
- **Most customers are "Loyal"** — 3,116 of them, compared to just 83 New and 701 Returning
- **Express shipping customers spend a little more** on average ($60.48 vs $58.46 for Standard)
- **Revenue is pretty evenly spread across age groups**, with Young Adults just slightly ahead

## The Dashboard

I built an interactive Power BI dashboard (`customer_behavior_dashboard.pbix`) so anyone could explore this data themselves — filter by subscription status, gender, category, or shipping type and see:

- Total customers, average purchase amount, and average rating at a glance
- Subscription breakdown
- Revenue and sales by category
- Revenue and sales by age group

*(Drop a screenshot of the dashboard here — e.g. `![Dashboard](images/dashboard.png)`)*

## What I'd recommend to the business

- Give subscribers real, exclusive perks to make signing up worth it
- Build a loyalty program to turn repeat buyers into truly "Loyal" customers
- Rethink the discount strategy — some products are too dependent on it
- Put top-rated, best-selling products front and center in marketing
- Focus marketing on high-revenue age groups and Express shipping users

## What's in this repo
