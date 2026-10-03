# Business Problem: AtliQ Hardware Business Compass 360 

> **Project:** AtliQ · **Type:** Guided project (Codebasics) · **Domain:** Computer hardware and consumer electronics
> **Stakeholders:** Executive management, Finance, Sales, Marketing, Supply Chain

---

## 1. Company and business model

**AtliQ Hardware** sells computer hardware such as PCs, mouse, keyboards and printers, in a model similar to HP or Dell. In the data, the portfolio is grouped into three divisions and six segments:

| Division | Segments |
|---|---|
| **PC** | Notebook, Desktop |
| **Peripherals & Accessories (P&A)** | Peripherals, Accessories |
| **Networking & Storage (N&S)** | Networking, Storage |

### Customers vs consumers

For AtliQ, the **customers** are the businesses that buy from it and resell (Croma, Best Buy, Amazon, Flipkart). The **consumers** are the end users, people like you and me.

### Two different ways to classify customers

These two dimensions are easy to mix up:

| Dimension | Values | Examples |
|---|---|---|
| **Customer type** | **Brick & mortar** (physical stores) · **Platform** (online marketplaces) | Croma, Best Buy · Amazon, Flipkart |
| **Sales channel** | **Retailer** · **Direct** · **Distributor** | see below |

**The three channels**

1. **Retailer:** third-party stores and marketplaces that buy from AtliQ and sell to consumers (Croma, Best Buy, Amazon, Flipkart and others).
2. **Direct:** AtliQ sells to consumers itself through **AtliQ Exclusive** stores and the **AtliQ e-Store**.
3. **Distributor:** used where selling directly to consumers isn't possible or practical (for example, in some countries such as China and South Korea). Distributors buy from AtliQ and supply other merchants.

### Geography

AtliQ reports in four regions: **APAC, EU, NA and LATAM**. These break down into seven sub-zones: India, ROA and ANZ (APAC); NE and SE (EU); NA; and LATAM.

*(ROA = Rest of APAC, ANZ = Australia and New Zealand, NE/SE = Northern/Southern Europe. I inferred these expansions from how the numbers reconcile, because the report's Info page doesn't define them.)*

---

## 2. Why this project exists

### The LATAM lesson

AtliQ has grown fast, but its expansion into **Latin America** went badly. The company tried to establish stores and a presence there and took heavy losses, because the decisions were based on **customer surveys and management intuition** rather than data.

### The strategic shift

In a new strategy meeting, **data analytics** became a top agenda item, with the goal of making **data-backed, transparent decisions**.

- The company used to analyse data in **Excel**. At today's scale, that approach doesn't hold up.
- A dedicated **data analytics team** was hired.
- Competitors such as **Dell**, a much larger company with a large analytics team, are putting pressure on AtliQ. The named competitors in this project's market-share data are *dale, innovo, pacer and bp*.

*Note on LATAM in the data:* in this dataset LATAM is small ($3.16M Net Sales in FY2021, 0.4% of the total) and roughly break-even. The LATAM story is the **motivation for the project**, and the dataset does not reproduce that loss. The same views (market-level P&L, sub-zone trends, forecast-risk flags) are what a market-entry review would need.

---

## 3. The core business problems

### A. Decisions based on intuition and disconnected Excel files
Without a shared source of truth, different teams can report different numbers for the same metric. Leadership needs one governed model where revenue, deductions, costs and forecasts reconcile.

### B. Rapid growth without profit
Evidence from the data (fiscal years run Sep–Aug):

| | FY2018 | FY2019 | FY2020 | FY2021 |
|---|---|---|---|---|
| Net Sales ($M) | 29.11 | 111.37 | 267.98 | 823.85 |
| Gross Margin % | 37.43 | 41.20 | 37.10 | 36.49 |
| Net Profit % | −4.4 | 2.2 | −0.9 | −6.6 |

Net Sales roughly doubled or tripled each year, yet FY2021 closed with a **net loss of −$54.65M**. Leadership needs to see *where* value is lost between gross price, deductions, cost of goods, and operating expense.

### C. Supply-chain mismatch
Forecast quality varies widely by customer, product and zone. Some areas carry **Excess Inventory** (working capital tied up, obsolescence risk). Others face **Out Of Stock** conditions, which means lost sales and lost share to competitors.

---

## 4. Business questions by function

| Function | Questions the solution must answer |
|---|---|
| **Finance** | What is the full waterfall from Gross Sales to Net Profit? Why is Net Profit negative when Gross Margin is healthy? How does performance compare with Last Year and with Target? |
| **Sales** | Which customers bring the most Net Sales and margin? How do Retailer, Direct and Distributor channels compare? Which markets combine high sales with strong margins? |
| **Marketing** | Which product segments are profitable, not just large? How much of the gross price is given away in pre- and post-invoice deductions? What are the unit economics? |
| **Supply Chain** | How accurate are forecasts and how is accuracy trending? Which customers, products and zones are at risk of excess inventory or stock-outs? Where is the largest absolute forecast error? |
| **Executive** | What are the top-level KPIs (Net Sales, GM %, NP %, Forecast Accuracy, Market Share)? What is the mix by division, channel and sub-zone? Who are the top customers and products? How is market share trending against competitors? |

---

## 5. Objectives and success criteria

| Objective | How I judged success |
|---|---|
| **One source of truth** | A single star-schema model where the P&L reconciles (Net Invoice Sales − deductions = Net Sales) and regions, segments and sub-zones add back to the company total. |
| **Self-service analysis** | Any page can be sliced by fiscal year, region, customer, product and channel, and compared against Last Year or Target. |
| **Actionable insight** | Each finding ends with a recommendation and a metric to track. |
| **Honest reporting** | Estimates, unvalidated inputs and data-quality issues are labelled instead of hidden. |

---

## 6. Scope

- **Time horizon:** FY2018–FY2022 Est. The fiscal year runs **September to August**. Sales data is loaded until **December 2021**, so FY2022 is 4 months of actuals plus an estimate.
- **Geography:** 4 regions, 7 sub-zones, country-level detail on the Sales page.
- **Granularity:** customer × product × month.
- **Deliverable:** an interactive Power BI report (Home, Finance, Sales, Marketing, Supply Chain, Executive, Info).

**Out of scope:** competitor internals (no Dell data), root-cause data outside the model (for example, how OpEx is spent), and redistribution of the raw dataset.

---

## 7. Assumptions and limitations

- **FY2022 is largely an estimate.** Targets exist **only for FY2022**, so "vs Target" comparisons can't be made for earlier years.
- **Operating expense, targets and market share come from manually curated flat files.** The loss story depends heavily on OpEx.
- Net Profit % is almost identical across product segments, which suggests OpEx is **allocated in proportion to sales** rather than tracked by product. Product-level profitability should be read with that in mind.
- Market share figures are not validated against an external source.

See [Approach.md](Approach.md#7-validation-and-limitations) for how these were handled, and [Key_Insights.md](Key_Insights.md) for the findings.
