
 
# Sales Performance Analysis

Excel dashboard analyzing revenue by production type, region, product category, and manager for Company A, built for Executive Management, Sales, and Operations teams.

### Problem to Be Solved

Build a decision-making dashboard to:

- Compare revenue from Self-production (Tự sản xuất) and Import (Nhập khẩu)
- Locate revenue concentration by province, product category, and time
- Compare manager performance
- Support adjustments to production, market, and product focus

Key questions

- What share of revenue comes from Self-production vs Import?
- How has monthly revenue trended for each production type?
- Which provinces contribute the most revenue?
- Which product categories are strongest in each production type?
- How do managers differ in Self-production and Import revenue?

## Table of Contents

- [I. Introduction](#i-introduction)
- [II. Design Thinking](#ii-design-thinking)
- [III. Visualization](#iii-visualization)
- [IV. Insight and Recommendation](#iv-insight-and-recommendation)
- [Tech Stack](#tech-stack)

## I. Introduction

### 1. Dataset

Transaction-level sales data, fiscal years 2020/21 and 2021/22. One flat table.

#### sales_transactions

| Column | Type | Description |
|---|---|---|
| Thời gian | DATE | Transaction date |
| Năm | STRING | Fiscal year (e.g. 2020/21) |
| Loại hình Sản xuất | STRING | Tự sản xuất / Nhập khẩu |
| Tỉnh/Thành | STRING | Province / city |
| Quản lý | STRING | Manager in charge |
| Mặt hàng | STRING | Product category (Nội thất, Đồng phục, Đồ nam...) |
| Khách hàng | STRING | Customer |
| Doanh số | FLOAT | Transaction revenue |

## II. Design Thinking

### Step 1: Empathize
[insert image]

### Step 2: Define POV
[insert image]

### Step 3: Ideate
[insert image]

### Step 4: Prototype and Review

Chart types matched to each question: pie for share of total, line for monthly trend, treemap for province ranking, column and bar for category and manager comparison, sparklines for trend per province. Slicers (Year, Province, Category) let users filter every chart.

## III. Visualization

### Sales Performance Dashboard

What does revenue look like?

- What share of revenue is Self-production vs Import?
- How has monthly revenue trended by production type?
- Which provinces contribute the most revenue?
- Which production type leads in the selected product category?
- How do managers compare by production type?

<img width="1415" height="633" alt="image" src="https://github.com/user-attachments/assets/1dd98dbd-fa49-41ba-99d9-c9ab9b3d2fbf" />

Insights

Screenshot filter: Năm 2020/21 and 2021/22, Tỉnh/Thành Đà Nẵng, Mặt hàng Phụ kiện. Values are read from the charts.

- Self-production is 69% of revenue and Import 31%.
- Monthly revenue is volatile: Self-production ranges roughly 3.5K to 9K, Import 2K to 5K. Both dip around year-end and peak in similar months, so the pattern looks seasonal. The trend does not show that either type grows faster.
- Hồ Chí Minh is the largest province, followed by Đà Nẵng, Hà Nội and Cần Thơ. Đồng Nai, Hải Phòng, Bình Phước and Hải Dương are small.
- In Phụ kiện, Self-production revenue (~115K) is about 2.2 times Import (~52K).
- Đăng Lâm has the highest Self-production revenue (~47K), ahead of Tùng Dương (~42K) and Tiến Dũng (~40K). Đăng Trà has Import revenue only (~19K). Tùng Dương has almost no Import (~3K).

## IV. Insight and Recommendation

| Insight | Recommendation |
|---|---|
| Self-production is 69% of revenue and Import 31%. | Protect Self-production capacity before peak months. Check margin by production type first, since revenue alone does not show profitability. |
| Revenue is volatile and both types move together, with year-end dips and shared peaks. | Plan production and stock around the seasonal cycle. Validate with at least two full years of monthly data. |
| Hồ Chí Minh is the largest province, followed by Đà Nẵng, Hà Nội and Cần Thơ. Other provinces are small. | Prioritize Hồ Chí Minh and Đà Nẵng for deeper penetration. Check customer concentration and growth per province before adding spend. |
| In Phụ kiện, Self-production revenue is about 2.2 times Import. | Pilot Phụ kiện in one weaker province and compare revenue per customer before scaling. |
| Đăng Lâm leads Self-production revenue. Đăng Trà sells Import only. Tùng Dương has almost no Import. | Compare managers by product mix and customer portfolio before sharing best practices, since gaps may come from portfolio rather than skill. |
| Import is the smaller channel (31%). | Use Import for category gaps and seasonal peaks. Compare Import share in peak and low months to confirm. |

## Tech Stack

- Excel (Pivot Table, Pivot Chart, Slicer, Sparkline, Treemap)

## Limitations

- Revenue only, no cost or margin data
- Dashboard values depend on active slicers
- No customer-level behavior data

## Repository Structure

.
├── README.md
├── sales_performance_dashboard.xlsx
├── data/
│   └── sales_transactions.csv
└── images/
    └── dashboard.png
