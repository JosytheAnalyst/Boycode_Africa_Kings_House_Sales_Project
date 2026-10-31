# BoyCode Africa — Kings House  
## Sales & Profitability Performance Review

**Portfolio Case Study**  
Simulated Nigerian E-commerce Dataset | Excel Analysis & Management Dashboard

---

### Business Problem
Management (Head of Commercial Operations) needs to understand what is driving revenue and profit, which products and categories deserve more commercial attention, and where the business should focus its sales effort. The goal is actionable recommendations based on clean evidence, not just charts.

### Dataset
- **Source:** BoyCodeAfrica Ecommerce_Dataset.csv (BoyCode Africa shared educational dataset)
- **Rows:** 1,812 raw records (including intentional duplicates)
- **Period:** Full year 2025 (simulated)
- **Core fields:** Order_ID, Order_Date, Customer_ID, Region, Customer_Segment, Category, Product, Quantity, Unit_Price, Discount, Revenue, Cost, Gross_Profit, Acquisition_Channel, Marketing_Cost, Payment_Method, Delivery metrics, Order_Status, Customer_Rating
- **Nature:** Synthetic data created for educational / portfolio purposes. Must be labelled as simulated when published.

### Data Preparation
Issues found and actions taken:

| Issue | Count / Detail | Action |
|-------|----------------|--------|
| Exact duplicate rows | 12 (appended at end of file) | Dropped duplicates, kept first occurrence → 1,800 unique orders |
| Missing Region | 10 rows | Filled with "Unknown" |
| Missing Acquisition_Channel | 7 rows | Filled with "Unknown" |
| Missing Customer_Rating | 314 (mostly Cancelled) | Left blank; ratings analysis restricted to completed orders with ratings |
| Date format | MM/DD/YYYY text | Converted to proper dates + YearMonth helper column |
| Customer_Segment | Already classified (New / Returning / Loyal) | Validated and used as-is |

Validation: Revenue, Discount_Amount and Gross_Profit relationships checked; no negative quantities/revenues/costs.

### Analysis
**Excel techniques used:**
- Excel Tables & structured references mindset
- Data cleaning & quality documentation sheet
- SUMIFS / aggregation logic (implemented via Python → Excel for reproducibility, equivalent formulas available)
- Date grouping (monthly trends)
- Pivot-style summaries for Category, Product, Region, Segment, Discount bands
- Conditional formatting (green = strong margin, red = weak margin)
- Line chart (monthly Revenue vs Gross Profit)
- Column chart (Revenue by Category)
- KPI cards and executive dashboard layout
- One-page management recommendation

**Key calculations:**
- Gross Margin % = Gross_Profit / Revenue
- Monthly trend tables
- Product ranking by Revenue, Gross Profit and Margin
- High-revenue / weak-margin flag (Margin < 25% and Revenue above median)
- Discount-band impact on margin
- Region and Customer Segment performance (including AOV)

### Key Findings
1. **Total Revenue:** ₦94.97 million | **Gross Profit:** ₦30.19 million | **Gross Margin:** 31.8% | **Orders:** 1,800 | **Units:** 2,945
2. Electronics and Home categories drive the largest share of revenue; selected Beauty and Fashion items often deliver stronger margins.
3. A clear set of Top-10 products combine high Gross Profit with healthy margin — these should receive priority commercial attention.
4. A set of high-revenue products sit below 25% margin and compress overall profitability; these require investigation (cost, pricing or discount depth).
5. Higher discount bands (especially 20%+) correlate with lower realised margins. Lagos, Abuja, Rivers and other major regions concentrate volume; Loyal and Returning segments show solid contribution.

### Recommendations
**Sell more of**
- Top-10 high-profit, healthy-margin products (see Category & Product sheet)
- Selected Electronics accessories and Beauty / Home items that clear the margin threshold
- Focus commercial and promotional effort on top-performing regions and Loyal / Returning segments

**Review / Investigate**
- Bottom-10 products by Gross Profit and any high-revenue SKUs with Margin < 25%
- Discount policy on already thin-margin items
- Supplier cost or pricing on high-volume low-margin lines
- Fix the 10 missing Region and 7 missing Channel records at source

**Immediate next steps (30–60 days)**
1. Align merchandising on the Top-10 list and set sales/promo priority  
2. Cost & pricing review on the weak-margin high-revenue list  
3. Tighten discount approval rules for SKUs below target margin  
4. Correct missing Region / Channel data in the source system  
5. Refresh this dashboard monthly and review with Commercial Ops weekly  

### Limitations
- Dataset is synthetic / educational; patterns may not generalise to live operations.
- Analysis is descriptive and correlational — it does not prove that changing any single lever (discount, assortment, region focus) will cause a specific outcome.
- Customer ratings are missing on most cancelled orders; full delivery & CX analysis belongs to Love & Light House.
- No formal customer LTV or multi-touch attribution model is included.

### Tools
Microsoft Excel (openpyxl-generated workbook with charts, conditional formatting, KPI cards and documented cleaning process)

### Deliverables in this Workbook
1. Executive Dashboard (KPI cards + monthly trend + category + region views)
2. Raw Data (preserved)
3. Cleaned Data
4. Data Cleaning Log (quality issues & actions)
5. KPI Summary + monthly trend chart
6. Category & Product analysis (rankings, high-revenue/weak-margin, Top 10 / Bottom 10)
7. Region & Segment + Discount impact
8. One-page Management Recommendations

---

**Author**  
Adewunmi Joseph  
Data Analysis Student  
BoyCode Africa  
Stellar Academy
