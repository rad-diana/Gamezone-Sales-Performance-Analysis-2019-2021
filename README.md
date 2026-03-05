# Gamezone Sales Performance Analysis (2019-2021)
## Backgroung and Overview
Gamezone, established in 2018, is a global e-commerce company that sells new and refurbished gaming products worldwide via its website and mobile app.

The company has significant amounts of data on its sales, marketing efforts, operational efficiency, and product offerings. This project thoroughly analyzes and synthesizes this data in order to uncover critical insights for finance, marketing and product teams that will improve Gamezone's commercial success. 

Insights and recommendations are provided on the following key areas:
- **Sales Trends Analysis**: Evaluation of historical sales patterns, both globally and by region, focusing on Revenue, Order Volume, and Average Order Value (AOV).
- **Product Level Performance**: An analysis of Gamezone's various product lines, understanding their impact on sales and returns.
- **Regional Comparisons**: An evaluation of sales and orders by region.

## Data Structure Overview
Gamezone's dataset as seen below consists of 2 tables: orders and region. 

Each unique record of the `orders` table corresponds to one purchase transaction, including information about the user, product, pricing, shipping, and marketing channel; for the `region` table - represents a country mapped to its corresponding geographical region.

<img width="960" height="510" alt="Gamezone ERD" src="https://github.com/user-attachments/assets/a08a5008-f114-4bcd-bea6-2c99e5e85b8a" />

Prior to beginning the analysis, a variety of checks were conducted for quality control and familiarization with the dataset, using Excel. You can find the initial and cleaned datasets, pivot tables for data checks and exploratory analysis, as well as isues log and insights log [here](link).

## Executive Summary
Between 2019 and 2021, the company generated approximately $6.1M in total revenue, with a significant acceleration beginning in early 2020. Sales more than doubled during the pandemic period, peaking in September and December 2020, before declining sharply in early 2021 toward pre-COVID levels.

Revenue growth was broad-based across products, regions, and channels, suggesting a macro-level demand surge driven by increased at-home gaming behavior. However, the analysis reveals structural concentration risks:

- A small set of products drives the majority of revenue and volatility: 27in 4K Gaming Monitor, Sony PS5 Bundle, and Nintendo Switch.
- The Direct marketing channel accounts for roughly 80% of sales, creating significant channel dependency.
- Revenue seasonality is heavily skewed toward Q4, with December consistently outperforming other months.

While the business proved highly responsive to favorable demand conditions, the post-2020 normalization highlights the need for diversification, improved forecasting stability, and reduced reliance on a narrow revenue base.

<img width="1652" height="1082" alt="gamezone dashboard 1" src="https://github.com/user-attachments/assets/8e031026-a27f-4a1d-a130-d06557588dc0" />
<img width="1652" height="572" alt="gamezone dashboard 2" src="https://github.com/user-attachments/assets/9d86a77e-d8cc-422f-9f54-d575837ebb5b" />

The entire interactive Tableau dashboard can be downloaded [here](link).

## Insights Deep Dive

### 1. Overall Sales Trends

Total sales across the observed period amount to approximately **$6.1M**, with monthly revenue fluctuating between roughly **$80K and $500K**. The most defining pattern in the dataset is the dramatic acceleration in 2020, followed by a sharp correction in early 2021.

Sales more than doubled in early 2020 and reached all-time highs in September and December 2020. However, revenue declined significantly in early 2021, dropping by more than half compared to peak months and approaching pre-COVID levels.

Importantly, this spike-and-dip pattern is consistent across Products, Regions, and Marketing channels.

This consistency strongly suggests **a macro-level demand driver** rather than isolated product or operational changes. The most likely explanation is pandemic-related consumer behavior shifts, particularly increased spending on home entertainment and gaming products.

The key takeaway from a Finance perspective is volatility. Revenue is highly sensitive to external demand cycles and seasonal spikes, which introduces forecasting risk and budgeting uncertainty.

### 2. Product Performance

- **The 27in 4K Gaming Monitor, Sony PlayStation 5 Bundle and Nintendo Switch** are the main revenue drivers. Gaming Monitor is the top-performing product, generating nearly **$2M** in total sales.
- **These three products also drive the 2020 spike and the early 2021 dip**. Their sales patterns closely mirror overall revenue trends, meaning total company performance is structurally tied to their lifecycle and demand cycles. 
- **The Razer Pro Gaming Headset** generated only around **$800** in total sales. Additionally, the headset category overall contributes **less than 2% of total revenue**.

<img width="1322" height="758" alt="gamezone product performance" src="https://github.com/user-attachments/assets/1f1b1956-f0a2-4a9a-96f3-84b82b8b8130" />

This creates two structural concerns:
- **Revenue concentration risk**: Performance depends disproportionately on three high-ticket items.
- **Portfolio inefficiency**: Low-performing categories may be occupying operational and marketing bandwidth without meaningful contribution.

### 3. Seasonality

**September and December months throughout 2019-2020 show a particularly large spike in sales** across almost all products. This may suggest strong holiday seasonality, potential promotional campaigns, and(or) heightened pandemic-driven demand during winter months. The fact that all products spiked simultaneously indicates coordinated or market-wide factors rather than isolated product promotions.

<img width="1149" height="759" alt="gamezone sales by month and product" src="https://github.com/user-attachments/assets/139c6921-2392-4258-a231-9234b23a02c9" />

### 4. Sales by Marketing Channel

**The Direct channel is the dominant revenue driver**, accounting for the vast majority of total sales (~ 80% of revenue). All other channels pale in comparison.

Additionally, the large dip in early 2021 is heavily driven by a decline in Direct channel revenue.

Top-3 products experienced a particularly strong drop in Direct traffic in early 2021 compared to other products and channels.

This raises important questions:
- Website discoverability changes?
- Inventory issues?
- Competitor availability?
- SEO ranking drop?
- Attribution over-reporting?

The key insight is that **heavy reliance on Direct traffic makes revenue vulnerable** to algorithm changes, technical issues, or competitive displacement.

<img width="1450" height="656" alt="gamezone sales by marketing channel" src="https://github.com/user-attachments/assets/3de875b1-9cd6-4667-984e-53db040f5ae1" />

### 5. Sales by Region

Sales trends are broadly similar across regions, reinforcing the macro-level nature of the 2020 spike and 2021 dip.

However, **North America** shows the steepest post-peak decline. Additionally, the **Sony PS5 drop** is particularly concentrated in North America and EMEA within the Direct channel (as it shows in a dashboard above).

Given North America's revenue weight, its volatility has an outsized impact on total sales performance.

<img width="1347" height="660" alt="gamezone sales by region" src="https://github.com/user-attachments/assets/858d799b-741b-4b91-ab90-9fb900bb771b" />

### 6. Refund Trends

Refund patterns closely follow revenue spikes, particularly during late 2020.

Top-revenue products (27in 4K Gaming Monitor, Nintendo Switch, and Sony PlayStation 5 Bundle) account for the largest refund volumes in absolute dollar terms. This mirrors the revenue concentration pattern. **The products driving revenue are also driving refund exposure**.

Key observations across products:
- The 27in 4K Gaming Monitor shows substantial refunded sales relative to its revenue size
- Nintendo Switch also exhibits a high refund count, consistent with its large order volume
- Sony PS5 Bundle shows high refund value, reflecting its high AOV
- Headsets generate low revenue but still show refund activity, which may indicate weaker customer satisfaction relative to sales size

Refund spikes are especially visible during the same months as revenue spikes, indicating that growth periods amplify operational and financial risk.

<img width="1320" height="759" alt="gamezone refunds" src="https://github.com/user-attachments/assets/4173e141-b58b-48c1-b74c-6a1323913008" />

## Recommendations

### 1. Reduce Product Concentration Risk (Product Team)

Since three products (the 27in 4K Gaming Monitor, Sony PlayStation 5 Bundle, and Nintendo Switch) drive the majority of revenue and volatility, to reduce reliance on them, the Product team should focus on:
- Expanding variations or premium tiers of top-performing products.
- Introducing complementary products that bundle with consoles and monitors.
- Reevaluating the headset category. Given its contribution of less than 2% of revenue, consider bundling strategies or discontinuation if performance does not improve.

### 2. Audit and Diversify Marketing Channels (Marketing Team)

Given Direct accounts for roughly 80% of revenue, to reduce reliance on this traffic and create a more balanced marketing strategy the Marketing Team should:
- Validate attribution logic to ensure Direct is not overstated (recommendation for the Data and Analytics Team).
- Strengthen email and other emerging channels showing potential.
- Reduce structural dependence on Direct over the next 1–2 years.

### 3. Leverage Q4 Seasonality Strategically (Marketing Team)

Given the strong December spike across all products to help maximize revenue during historically strong periods:
- Begin promotional ramp-up in October.
- Allocate higher marketing budgets to November and December.
- Prioritize Gaming Monitor, Nintendo Switch, and Sony PS5 in winter campaigns.

### 4. Strengthen North America Recovery Strategy (Marketing Team)

Given NA shows the steepest dip:
- Conduct competitive pricing analysis.
- Evaluate inventory constraints during early 2021.
- Launch targeted campaigns for top-performing products in NA.

### 5. Implement Refund Risk Controls (Finance Team, Product Team, Customer Experience Team)

Since refund exposure is concentrated in high-ticket items:
- The Product team should ensure product pages contain clear specifications, compatibility information, and setup guidance to reduce misunderstanding before purchase.
- The Customer Experience team should strengthen post-purchase support, helping customers resolve issues before they decide to return products.
- The Finance team should begin tracking refund rates as a recurring KPI, rather than monitoring only the total refunded value.
