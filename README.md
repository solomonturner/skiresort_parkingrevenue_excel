# Ski Resort Parking Revenue Analysis (Excel)
**Tools Used:** Microsoft Excel (Power Query, IF/IFS, PivotTables, PivotCharts)
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
  - Pricing Policy
<img width="1729" height="803" alt="image" src="https://github.com/user-attachments/assets/27b24e0e-f5af-41e1-9fdd-10ecc0b892d5" />

## Methodology & Exploratory Data Analysis (EDA)

Excel was the only tool used for this analysis, from combining and cleaning the raw files to building the visualizations below. Two key patterns emerged early:
- A **significant decline in parking revenue** beginning at the start of the 2024/25 season.
- The **majority of premium parkers visited the paid lot only once** during an entire ski season, suggesting the program primarily serves day-trip visitors rather than repeat local traffic.

The **2024/25 season** stands out as the clearest outlier. The significant decline suggests an external factor may have influenced results rather than either pricing model alone. Confirming the cause would require additional data beyond parking transactions, such as overall mountain visitation figures for the same period.

## Key Findings & Visualizations

<img width="1664" height="654" alt="skiresort_dashboard_gif" src="https://github.com/user-attachments/assets/955084bc-9132-45cb-91a2-ef86251a9ba9" />

**Headline metrics (all seasons combined):**

| Metric | Value |
|---|---|
| Total Parking Sessions | 1,045 |
| Average Parking Duration | 1.17 days |
| Average Revenue Per Parker | $27.62 |

**Revenue and Parking Sessions by Month**

Revenue and session volume tell the same story. During the 2023/24 season, the only full season with all-week paid parking, monthly revenue peaked at roughly $5,000 to $7,000, with parking sessions tracking closely alongside it. Parking revenue and session volume started off cold (pun intended) in the 2024/25 season. On January 17, partway through the season, the pricing model changed from daily paid parking to weekends and holidays only. Both revenue and session volume declined following the change and never recovered to prior levels, even during the following full season (2025/26), when weekends-and-holidays-only pricing was in effect for the entire year.

**New vs. Returning Parkers by Season**

| Season | New Parkers | Returning Parkers | Total |
|---|---|---|---|
| 2023/24 (all-season paid parking) | 353 | 178 | 531 |
| 2024/25 (mid-season pricing change) | 69 | 64 | 133 |
| 2025/26 (full season, weekends/holidays only) | 242 | 139 | 381 |

Two things stand out here:

1. The **2023/24 season significantly outperformed** both later seasons across new and returning parkers. This was the only full season with all-week paid parking, suggesting that weekday paid parking may have contributed to higher parking adoption and revenue capture. However, external factors such as overall mountain visitation, snowfall, or operating conditions may have also influenced the results.
2. The **2024/25 season appears to be the primary outlier**, while 2025/26 shows signs of recovery toward the volume trends observed in 2023/24. Total sessions increased from 133 in 2024/25 to 381 in 2025/26, indicating that demand returned closer to 2023/24. The remaining gap compared to 2023/24 may be explained by the loss of weekday paid parking revenue outside of holidays, rather than a significant decline in parking demand. This hypothesis would require further analysis and is explored later in this report.

## Limitations & Next Steps

This analysis was conducted using parking data alone, which required several assumptions based on domain knowledge of ski resort and parking operations rather than confirmed through external data sources. Most importantly, paid parking is not the resort’s primary revenue driver. Lift passes, on-mountain purchases, and rentals contribute significantly more to overall resort revenue.

To better understand the changes observed in parking revenue, additional data would be required to determine whether the decline in parking sessions over the past two seasons reflects broader changes in mountain visitation or whether the shift from all-season paid parking to weekends-and-holidays-only pricing contributed to the decline.

**Next steps:**

- Acquire mountain-wide visitation data (season passes sold, daily lift tickets issued, skier visits, etc.) to separate broader visitation trends from parking-specific behavior.
- Conduct a like-for-like comparison between the 2023/24 and 2025/26 seasons by isolating the impact of non-holiday weekday parking. This would involve removing non-holiday weekday bookings from the 2023/24 season to estimate how revenue and session volume compare under a similar weekends-and-holidays-only model.
- Look for a potential increase in mountain visits on non-holiday weekdays during the 2025/26 season to see if the resorts primary revenue source increased.

**Domain-knowledge-based recommendation (pending further analysis):** The key decision is not whether paid parking should exist, but rather which pricing model best captures revenue while supporting mountain operations. Because there is no fixed monthly platform cost associated with operating the program, paid parking provides additional revenue while also helping manage traffic flow and congestion by encouraging visitors to utilize the appropriate parking areas. Given the overall cost of a ski trip, including equipment, lift tickets, travel, and accommodations, an additional ~$25 parking fee is unlikely to be the primary deciding factor for most visitors.

Further analysis of mountain-wide visitation data and weekday parking demand will help determine whether all-season pricing or weekends-and-holidays-only pricing provides the best balance between revenue generation, visitor experience, and operational efficiency.
