# Ski Resort Parking Revenue Analysis (Excel)

## Executive Summary

After the 2025/26 ski season, a North American ski resort sought to evaluate the effectiveness of its premium paid parking program. The analysis focused on two key business questions:
1. Was parking revenue higher when paid parking was in effect throughout the season (weekdays and weekends) compared with the later policy of charging only on weekends and holidays?
2. Does the paid parking program continue to provide sufficient business value to justify its operation?

While the pricing policy change may have contributed to the decline, the available parking data alone cannot establish a causal relationship. Other factors were outside the scope of this initial exploratory analysis but would be required to determine the underlying cause of the decline, including snowfall conditions, season pass sales, daily lift ticket sales, and overall mountain visitation.

Despite the reduction in revenue, the paid parking program continues to generate meaningful income with minimal operating costs, suggesting that discontinuing the program would likely forgo revenue without providing a significant financial benefit. Based on the available evidence, maintaining the paid parking program is the recommended course of action.

## Project Context & Objectives

As a Business Development professional in the parking software industry, I manage a portfolio of client accounts, including a North American ski resort. During the 2023/24 ski season, the resort introduced a premium paid parking program for the lot closest to the ski lifts. The program was designed to generate additional parking revenue while improving traffic flow and reducing congestion by positioning the premium lot as the closest and most convenient parking option. Visitors who chose not to pay were directed to a free parking lot located closer to the base of the mountain.

Paid parking launched in the 2023/24 ski season. By the end of 2025/26, the client was questioning whether the program was worth continuing, largely due to a visible decline in parking revenue since launch. Specifically, they wanted to know:

1. Was parking revenue higher when paid parking was in effect throughout the season (weekdays and weekends) compared with the later policy of charging only on weekends and holidays?
2. Does the paid parking program continue to provide sufficient business value to justify its operation?

The results of this analysis will help determine whether the client continues operating the paid parking program and inform future pricing decisions. An important consideration is that the parking software is priced as a percentage of parking revenue rather than a fixed fee, meaning the resort incurs no fixed operating cost to run the paid parking program.

## Data Sourcing & Preparation

Data was sourced directly from the parking software platform used by the client, exported as 20 separate Excel files covering the three ski seasons in scope. The raw data was generally clean, but required consolidation before analysis:

- **Combined** all 20 files into a single working dataset
- **Standardized date formatting** across files
- **Added derived fields via IF statements** to support trend analysis, including:
  - Ski Season (2023/24, 2024/25, 2025/26)
  - New vs. Returning Parker
  - Total Parking Duration
<img width="1729" height="803" alt="image" src="https://github.com/user-attachments/assets/27b24e0e-f5af-41e1-9fdd-10ecc0b892d5" />

## Methodology & Exploratory Data Analysis (EDA)

Excel was the only tool used for this analysis — from combining and cleaning the raw files to building the visualizations below. Two patterns emerged early:

- A **drastic decline in parking revenue** starting partway through the 2024/25 season
- The **majority of premium parkers visited the paid lot only once** across an entire ski season, suggesting the program serves mostly occasional/day-trip visitors rather than repeat local traffic

The **2024/25 season stands out as the clearest outlier**. The scale of the drop points to an external factor rather than the pricing model itself, but confirming that would require data beyond parking transactions alone — such as overall mountain visitation for the same period.

## Key Findings & Visualizations

<img width="1664" height="654" alt="skiresort_dashboard_gif" src="https://github.com/user-attachments/assets/955084bc-9132-45cb-91a2-ef86251a9ba9" />

**Headline metrics (all seasons combined):**

| Metric | Value |
|---|---|
| Total Parking Sessions | 1,045 |
| Average Parking Duration | 1.17 days |
| Average Revenue Per Parker | $27.62 |

**Revenue and Parking Sessions by Month**

Revenue and session volume tell the same story. During the 2023/24 season — the only full season of all-week paid parking — monthly revenue peaked at roughly $5,000–$7,000 with parking sessions tracking closely alongside it. On **January 17**, mid-way through the 2024/25 season, the pricing model changed from daily paid parking to **weekends and holidays only**. From that point forward, both revenue and session volume dropped sharply and never recovered to prior levels, even in the following full season (2025/26), when weekends-and-holidays-only pricing was in effect for the entire year.

**New vs. Returning Parkers by Season**

| Season | New Parkers | Returning Parkers | Total |
|---|---|---|---|
| 2023/24 (all-week paid parking) | 353 | 178 | 531 |
| 2024/25 (mid-season pricing change) | 69 | 64 | 133 |
| 2025/26 (full season, weekends/holidays only) | 242 | 139 | 381 |

Two things stand out here:

1. **2023/24 significantly outperforms both later seasons** on new and returning parkers alike — well before any pricing change occurred, which points to something else driving overall parking demand that year.
2. **2025/26 recovered meaningfully from the 2024/25 trough** (381 vs. 133 total parkers) but still fell well short of 2023/24 levels, even though 2025/26 ran the same weekends-and-holidays-only model for the full season that 2023/24 ran daily paid parking.

Taken together, the pricing change alone does not explain the shape of the trend — a full, clean season of weekends-only pricing (2025/26) did not outperform a full season of daily pricing (2023/24), but it also didn't need to "catch up" to 2023/24 to be considered a reasonable model, since 2024/25's collapse looks driven by something outside the parking program itself.

## Limitations & Next Steps

This analysis was conducted on parking data alone, which required a number of assumptions grounded in domain knowledge of ski resort and parking operations rather than confirmed by outside data. Most importantly: paid parking is not the resort's primary revenue driver — lift passes and on-mountain purchases/rentals are, so it's important to assess whether the drop in parking sessions over the past two seasons reflects lower overall mountain visitation, or a genuine drop-off in appetite for paid parking specifically.

**Next steps:**

- Acquire mountain-wide data (season passes sold, daily lift tickets issued, etc.) to separate visitation effects from parking-specific effects
- Isolate non-holiday weekday bookings within the 2023/24 season, remove them, and compare like-for-like revenue and session counts between 2023/24 and 2025/26 before making a final call on which pricing model performs better
- Revisit this analysis once mountain visitation data is available to confirm (or rule out) the 2024/25 season as an external-event-driven outlier

**Domain-knowledge-based recommendation (pending further analysis):** Continue the parking program. There is no monthly platform cost, and the offering has clear value to both the resort (traffic and congestion management) and to visitors. Ski trips are high-ticket by nature, and an incremental ~$25 parking charge is unlikely to be the deciding factor for a visitor who is already budgeting for equipment, lift tickets, travel, and accommodations.
