# Key Business Insights: AtliQ Business Compass 360

> **Source:** my Power BI report (Finance, Sales, Marketing, Supply Chain, Executive views). Every number comes from the dashboard, or is a simple calculation from dashboard numbers (marked *derived*).

---

## How to read these numbers

- **Fiscal year = September to August.** FY2021 = Sep 2020–Aug 2021 and is the **last fully actual year**.
- **FY2022 Est = 4 months of actuals (Sep–Dec 2021) + an 8-month estimate.** FY2022 findings are hypotheses to test, not results.
- **BM (benchmark)** is Last Year unless a section says "vs Target". Targets exist only for FY2022.
- Dollar values are in millions ($M). Net Error and ABS Net Error are in **units** (forecast quantity minus sales quantity).
- Where the dashboard shows relative change on a negative base, I describe it in percentage points instead.

### Scorecard

| | FY2018 | FY2019 | FY2020 | FY2021 | FY2022 Est |
|---|---:|---:|---:|---:|---:|
| Net Sales ($M) | 29.11 | 111.37 | 267.98 | 823.85 | 3,736.17 |
| Net Sales growth vs LY | n/a | +282.57% | +140.61% | +207.43% | +353.5%* |
| Gross Margin % | 37.43 | 41.20 | 37.10 | 36.49 | 38.08 |
| Operational Expense | -12.17 | 43.43 | -101.71 | -355.28 | -1945.30 |
| Net Profit ($M) | −1.28 | 2.46 | −2.29 | −54.65 | −522.42 |
| Net Profit % | −4.38 | 2.21 | −0.85 | −6.63 | −1  3.98 |
| Forecast Accuracy | 80.31% | 86.45% | 72.99% | 80.21% | 81.17%* |

\* Estimate-based or unvalidated; see sections 6 and 7.

**The story in one paragraph:** AtliQ's sales grew about 28x between FY2018 and FY2021, and gross margin held at 36–41%. But operating expense grew faster than gross margin, so the company went from a small profit (FY2019) to a −$54.65M loss (FY2021). The leaks are three-fold: (1) heavy deductions that leave only about half of the gross price as Net Sales, (2) operating expense concentrated in a few zones (India above all), and (3) forecasting that has swung from over-stocking to stock-outs as growth accelerated.

---

## 1. Growth is not turning into profit (Finance)

**Finding:** Gross margin is stable, so the problem sits **below** the gross-margin line.

**Evidence: FY2021 P&L waterfall ($M)**

```
Gross Sales                          1,664.64
  − Pre-invoice deductions            −392.50   (23.6% of Gross Sales)
Net Invoice Sales                    1,272.13
  − Post-invoice discounts            −281.64   (16.9%)
  − Post-invoice other deductions     −166.65   (10.0%)
Net Sales                              823.85   (49.5% of Gross Sales)
  − Manufacturing cost                −497.78
  − Freight cost                       −22.05
  − Other cost                          −3.39
Total COGS                            −523.22   (63.5% of Net Sales)
Gross Margin                           300.63   (36.49%)
  − Operational expense               −355.28   (43.1% of Net Sales)
Net Profit                             −54.65   (−6.63%)
```

- Operating expense exceeded gross margin by **$54.65M**, which is exactly the net loss.
- Manufacturing is the dominant COGS item (95.1% of COGS in FY2021). Freight is small (about 2.7% of Net Sales).
- OpEx exceeded gross margin in FY2018, FY2020, FY2021 and FY2022 Est. **FY2019 was the only profitable year**, when OpEx (39.0% of sales) was below gross margin (41.2%).
- The loss is growing faster than sales: net loss went from −$2.3M (FY2020) to −$54.7M (FY2021), about 24x, while sales grew about 3x.
- *FY2022 Est:* OpEx is estimated at $1,945M against gross margin of $1,423M, a −$522M gap. Net Profit % falls 7.4 pts, entirely because OpEx rises from 43.1% to 52.1% of sales while gross margin improves 1.6 pts.

**Seasonality (read from the monthly trend):** Net Sales peak every year in November–December, then drop roughly 45–60% in January and stay flat until the next peak. The flat January–August line appears in completed years too, which is a feature of the dataset worth documenting.

**So what:** Raising sales will not fix this. At the estimated FY2022 gross margin of 38.08%, breaking even would require OpEx to fall by about $522M (about 27%). *(arithmetic, not a forecast)*

**Recommendation:** Make OpEx, not gross margin, the first management priority, and get OpEx by zone (see section 5).

---

## 2. Only about half of the gross price becomes Net Sales (price realization)

**Evidence** *(derived: Gross Sales = Net Invoice Sales + Pre-invoice deductions)*

| Fiscal year | Gross Sales ($M) | Pre-invoice (% of gross) | Post discounts | Post other deductions | **Net Sales kept** |
|---|---:|---:|---:|---:|---:|
| FY2018 | 58.32 | 23.9% | 18.3% | 7.9% | **49.9%** |
| FY2019 | 209.06 | 22.7% | 14.2% | 9.8% | **53.3%** |
| FY2020 | 535.94 | 23.3% | 17.9% | 8.9% | **50.0%** |
| FY2021 | 1,664.64 | 23.6% | 16.9% | 10.0% | **49.5%** |
| FY2022 Est | 7,370.14 | 23.4% | 16.9% | 9.0% | **50.7%** |

- In FY2021, deductions took **$840.79M**, more than half of gross price.
- **FY2019 retained the most (46.72%) and also had the best gross margin (41.2%)** with the lowest discounts. This is consistent with discount depth driving margin, though one year isn't proof.

**Recommendation:** Review discount and deduction policy by customer, and move from unconditional discounts toward performance-based, tiered rebates. 

---

## 3. Customers and channels (Sales)

**Finding:** Margin depends on **who** buys, not **what** they buy.

**Top customers, FY2021 (actual)**


| Customer        | Channel  | Net Sales ($M) | Gross Margin ($M) |       GM % |
| --------------- | -------- | -------------: | ----------------: | ---------: |
| Amazon          | Retailer |         109.03 |             38.59 |     35.40% |
| AtliQ Exclusive | Direct   |          79.92 |             34.95 | **43.73%** |
| AtliQ e-Store   | Direct   |          70.31 |             26.40 |     37.54% |
| Sage            | Retailer |          27.07 |              9.52 |     35.16% |
| Flipkart        | Retailer |          25.25 |              7.64 | **30.23%** |
| Leader          | Retailer |          24.51 |              8.34 |     34.01% |
| Neptune         | Retailer |          21.00 |              8.65 |     41.17% |
| Ebay            | Retailer |          19.87 |              7.17 |     36.10% |


Company GM % in FY2021 was 36.49%.

- **Concentration:** Amazon + AtliQ Exclusive + AtliQ e-Store were 31.5% of FY2021 sales. Their combined share was 32.6%, 32.5%, 39.0%, 31.5% and 31.1% across FY2018–FY2022 Est. The top 5 customers' combined share was 43.7%, 43.0%, 46.2%, 37.8% and 38.2%.
- **Amazon is the largest account but dilutes margin.** It was above the company GM % through FY2020, but below it in FY2021 (35.40% vs 36.49%) and FY2022 Est (36.78% vs 38.08%).
- **AtliQ Exclusive is the margin leader**, at about 44–48% in every year. The AtliQ e-Store, though, earns roughly the company average (37.5% in FY2021), so "Direct" is not uniformly high-margin.
- **Unstable margins:** Leader fell from 48.1% (FY2019) to 26.4% (FY2020). Sage swung between 25.6% and 43.7%. Flipkart slid from 38.9% (FY2018) to 30.2% (FY2021), then shows 42.1% in the FY2022 estimate.
- **Channel mix** (share of Net Sales):

|Channel | FY2018 | FY2019 | FY2020 | FY2021 | FY2022 Est |
|---|---:|---:|---:|---:|---:|
| Retailer | 67.7% | 66.0% | 68.8% | 70.6% | 71.5% |
| Direct | 18.6% | 18.8% | 20.4% | 18.2% | 17.8% |
| Distributor | 13.7% | 15.3% | 10.8% | 11.2% | 10.7% |

  The business is becoming more retailer-dependent.

**Recommendations**

1. Review terms with Amazon and Flipkart (and Leader and Sage). **Track** GM % by customer vs the company average.
2. Find out *why* AtliQ Exclusive earns 44–48%. A plausible hypothesis is lighter deductions, which the data should confirm before expanding direct stores.
3. Watch concentration: three accounts supply about a third of sales.

---

## 4. Products and segments (Marketing)

**FY2021 (actual)**

| Segment | Net Sales ($M) | GM % | Net Profit ($M) | NP % |
|---|---:|---:|---:|---:|
| Notebook | 266.49 | 36.45 | −17.71 | −6.6 |
| Accessories | 244.85 | 36.47 | −16.28 | −6.7 |
| Peripherals | 166.51 | 36.52 | −11.02 | −6.6 |
| Storage | 54.42 | 36.75 | −3.46 | −6.4 |
| Desktop | 46.43 | 36.17 | −3.27 | −7.0 |
| Networking | 45.16 | 36.75 | −2.91 | −6.4 |

- **Uniform margins:** all six segments earn 36.2–36.8% gross margin, and their net profit % is within 0.6 pts of each other. 
- **Divisions, FY2021:** P&A 49.9%, PC 38.0%, N&S 12.1% of Net Sales.
- **The mix is shifting to PCs.** PC is 61.3% of FY2022 Est sales (Notebook 42%, Desktop 19%). N&S falls from 28.0% (FY2019) to 2.5%, with Networking down 15% in FY2022 Est and Storage flat (about $95M combined since FY2021).
- **Desktop** Net sales went from $0.95M (FY2020) to $46.4M (FY2021)
- **Short product life cycles:** the top-5 products' combined revenue share fell from 34.8% (FY2019) to 16.3% (FY2021) and 23.2% (FY2022 Est), and the top products change almost every year (apart from successor models such as BZ Allin1 → BZ Allin1 Gen 2). That makes forecasting harder.

**Recommendation:** Look for savings in cost structure and discounts, not in a single product line. Ask Finance how OpEx is allocated before cutting or expanding any segment.

---

## 5. Geography: where the loss sits (Executive and Marketing)

**FY2021 by region (actual)**

| Region | Net Sales ($M) | Share | GM % | Net Profit ($M) | NP % |
|---|---:|---:|---:|---:|---:|
| APAC | 441.98 | 53.6% | 35.34 | −33.33 | −7.5 |
| EU | 200.77 | 24.4% | 38.34 | +2.81 | +1.4 |
| NA | 177.94 | 21.6% | 37.23 | −24.32 | −13.7 |
| LATAM | 3.16 | 0.4% | 37.54 | +0.20 | +6.2 |
| **Total** | **823.85** | 100% | 36.49 | **−54.65** | −6.6 |

**Recommendations**
1. Prioritize APAC and NA for profitability improvement. Review OpEx, pricing, discounts, and cost allocation, as both regions are loss-making despite strong sales.
2. Improve APAC margins. With 53.6% of sales but only 35.34% GM and −7.5% NP%, investigate margin and operating-cost drivers.
3. Investigate NA separately. NA has 37.23% GM but −13.7% NP%, indicating significant costs below gross profit.
4. Use EU as a benchmark and evaluate LATAM cautiously due to its very small 0.4% sales contribution.

---

## 6. Forecast accuracy and inventory risk (Supply Chain)

*Positive Net Error = over-forecast (Excess Inventory risk). Negative = under-forecast (Out Of Stock risk). Units, not dollars.*

| Fiscal year | Forecast Accuracy | Change vs LY (pts) | Net Error (K units) | Net Error % | ABS Net Error (M units) | Risk |
|---|---:|---:|---:|---:|---:|---|
| FY2018 | 80.31% | n/a | +677.9 | +16.41% | Excess Inventory |
| FY2019 | 86.45% | +6.1 | +637.5 | +5.58% | Excess Inventory |
| FY2020 | 72.99% | −13.5 | +491.6 | +2.31% | Excess Inventory |
| FY2021 | 80.21% | +7.2 | −751.7 | −1.52% | Out Of Stock |
| FY2022 Est* | 81.17% | +1.0 | −3,472.7 | −9.48% | Out Of Stock |

**Recommendations**

1. Prioritize Peripherals, which drives ~92% of FY2022 Est. net under-forecast. Review its demand signals and forecasting separately.
2. Monitor customer × product × month accuracy, using both Forecast Accuracy and ABS Net Error to expose offsetting errors.
3. Rebalance inventory by zone, especially from Excess Inventory in NA/LATAM toward Out-of-Stock zones, while validating demand before transfers.
4. Review low-accuracy customers such as Sorefoz, Euronics, and UniEuro, and investigate the FY2020 shock and subsequent forecast-bias shift.

---

## 7. Market share and competition (Executive)

| | FY2018 | FY2019 | FY2020 | FY2021 | FY2022 Est |
|---|---:|---:|---:|---:|---:|
| AtliQ | 0.0% | 0.2% | 0.4% | 1.1% | 5.9% |
| dale | 25.7% | 22.4% | 22.8% | 21.8% | 22.3% |
| innovo | 11.2% | 10.1% | 10.2% | 9.6% | 9.9% |

*(bp and pacer each hold roughly 7–9% in every year. Values were read from the chart.)*

- AtliQ is a small player (1.1% share in FY2021) next to the leader, dale, at about 22%.
- The jump to 5.9% in FY2022 Est comes with no loss of share by the named competitors, so it would have to come from other brands, or the estimate is optimistic. It also shows the same 5.9% in every sub-zone, so I **treat it as unvalidated** until the manual market-share file is checked.

**Recommendation:** Validate the market-share file (units vs revenue, coverage), then use it to judge whether growth is share gain or market growth.

---

## 8. Data quality and caveats

- **FY2022 Est is mostly projection** (4 actual months). Growth of +353.5%, the −$522M loss, zone flips, the PC mix and the 5.9% market share all inherit this.
- **No target data before FY2022.** The report shows "BM Target(s) is not available" for FY2018–FY2021 when Target is selected, by design.
- **Target comparison:** FY2022 Est Net Sales is $3,736.17M vs Target $3,807.09M (−1.86%), Gross Margin % 38.08% vs 38.34%, Net Profit % −14.0% vs −14.19%. The planned loss was already about −14%, and the green status only means "slightly better than plan", not "healthy". A gap this small may simply reflect how the estimate was built.
- **OpEx, targets and market share are manual inputs.** The conclusions about the loss rest on OpEx, so its owner and method need confirming.
- **Relative changes on small or negative bases** (Desktop +4,791%, Net Profit % variances) are mathematically valid but misleading. I used percentage points where possible.
- **Scatter charts** may filter out some points (for example, the FY2019 country view). Country readings are approximate.
.


