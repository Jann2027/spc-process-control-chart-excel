# Statistical Process Control (SPC) Chart in Excel

A process-monitoring project that applies Statistical Process Control to **[METRIC, e.g. pH readings]** from **[DATASET NAME, e.g. Water Potability dataset]**, using control limits and Nelson's rules to detect out-of-control points and support quality decisions.

---

## Objective

To monitor a process measurement over time, separate normal variation from special-cause variation, and flag points that need investigation, the way a quality control engineer monitors a production process.

## Dataset

- **Source:** [DATASET NAME AND LINK]
- **Metric analysed:** [METRIC]
- **Records used:** [NUMBER OF READINGS]
- **Time axis:** [DATE / SAMPLE NUMBER]

## Tools Used

- Microsoft Excel (formulas, conditional logic, charting)
- Functions: `AVERAGE`, `STDEV.S`, `IF`, `ABS`, `AND`

## Method

1. Cleaned and arranged the data in two columns: date/sample and measured value.
2. Calculated the **centre line** (overall mean) and **standard deviation**.
3. Plotted the data as a line chart with the centre line and **±1σ, ±2σ and ±3σ control zones**.
4. Applied **Nelson's rules** to flag unusual points:
   - **Rule 1:** one point more than 3σ from the mean
   - **Rule 2:** nine or more points in a row on the same side of the mean
   - **Rule 3:** six or more points continually increasing or decreasing
5. Highlighted flagged points in red on the chart.
6. Reviewed each flagged point and tested how removing a confirmed outlier changes the mean and control limits.

## Key Findings

- The process mean was **[MEAN]** with a standard deviation of **[STD DEV]**.
- **[NUMBER]** points violated **[RULE NUMBERS]**, mainly around **[DATES / SAMPLE NUMBERS]**.
- Removing the outlier on **[DATE]** changed the mean from **[X]** to **[Y]**.
- Possible causes to investigate: **[e.g. sensor error, change in source, sampling issue]**.
- Recommendation: **[e.g. recheck the process on the flagged dates and monitor closely when a trend appears]**.

![Control chart](screenshots/control-chart.png)

## How to Use

1. Open `SPC_Control_Chart.xlsx`.
2. Enter or paste data into the **Date** and **Metric Value** columns.
3. Turn rules on or off using `TRUE` / `FALSE`.
4. Review the points flagged on the chart.
5. Add confirmed outliers to the **Outliers** table to recalculate the limits.

## Key Learnings

- The difference between normal variation and special-cause variation.
- How control limits (±3σ) are calculated and what a violation means.
- Why trends and runs (Rules 2 and 3) matter even when no point crosses the limit.
- A control chart shows **what** happened, not **why**; finding the root cause needs further investigation.

## Limitations

- Based on a public dataset, not data from a live plant process.
- Control limits use the overall mean and standard deviation of the full dataset.

