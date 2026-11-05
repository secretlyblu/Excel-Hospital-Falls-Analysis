# Hospital Falls Baseline Report | Excel Project

## Project Overview

**Project Title**: Hospital Falls Baseline Report (Falls Prevention Program)
**Level**: Beginner
**Tool**: Microsoft Excel (Tables, PivotTables, Filters, Date Grouping)
**Dataset**: Synthetic hospital falls log (60 falls, January 2024 to June 2025). No real patient information is used.

This project demonstrates how a healthcare analyst can use Excel to turn a raw incident log into a clear baseline report. A hospital is launching a falls prevention program and needs to know how many falls happened each quarter, and how many were assisted versus unassisted, before the program begins.

## Business Problem

The AVP of Nursing at Hospital 1 is launching a Falls Prevention Program on **Unit B**. Before the program starts, leadership needs a **baseline** to measure future improvement against. They asked for:

- The number of falls **per quarter** from January 2024 through June 2025
- How many of those falls were **assisted** versus **unassisted**

## Objectives

1. **Organize the data**: Convert the falls log into an Excel Table so the analysis updates as data is added.
2. **Scope the analysis**: Limit the report to Hospital 1, Unit B, the unit and hospital launching the program.
3. **Summarize with a PivotTable**: Count falls by quarter and fall type.
4. **Report the baseline**: Present clear results leadership can use to track the program's impact.

## Dataset

The data lives in the `Scenario 1 - Falls` sheet as an Excel Table named **FallsData** (60 rows).

| Column | Description |
|---|---|
| Fall ID | Unique ID for each fall (F001 to F060) |
| Fall Date | Date the fall occurred |
| Hospital | Hospital 1 or Hospital 2 |
| Unit | Unit A, Unit B, or Unit C |
| Fall Type | Assisted (staff present) or Unassisted |

**Data quality check**: No blank cells, and every Fall ID is unique, so no cleaning was needed.

## Approach

1. **Create an Excel Table.** The data range was formatted as a Table (`FallsData`) so formulas and PivotTables grow with new records.
2. **Insert a PivotTable** from `FallsData` on the `S1 - Pivot` sheet.
3. **Set up the PivotTable fields:**
   - **Filters:** Hospital = Hospital 1, Unit = Unit B
   - **Rows:** Fall Date, grouped by **Years and Quarters**
   - **Columns:** Fall Type
   - **Values:** Count of Fall ID
4. **Group dates by Years and Quarters.** Right-click a date in the PivotTable, choose **Group**, and select both **Years** and **Quarters**. Grouping by quarters alone would combine the same quarter from different years (for example, Q1 2024 and Q1 2025).
5. **Add grand totals** and review the results against the raw data.

## Results

**Baseline for Hospital 1, Unit B (January 2024 to June 2025)**

| Quarter | Assisted | Unassisted | Total Falls |
|---|---|---|---|
| 2024 Q1 | 3 | 3 | 6 |
| 2024 Q2 | 4 | 2 | 6 |
| 2024 Q3 | 4 | 2 | 6 |
| 2024 Q4 | 4 | 2 | 6 |
| 2025 Q1 | 3 | 2 | 5 |
| 2025 Q2 | 4 | 2 | 6 |
| **Total** | **22** | **13** | **35** |


<img width="652" height="315" alt="image" src="https://github.com/user-attachments/assets/a28bafd2-4eb9-4a69-9e5a-cd0bff92617f" />

## Findings

- **Baseline volume:** Unit B at Hospital 1 had **35 falls** over six quarters, an average of about **5.8 falls per quarter**. The count is very stable, ranging from 5 to 6 per quarter.
- **Assisted vs. unassisted:** **22 falls (62.9%)** were assisted and **13 (37.1%)** were unassisted.
- **Assisted falls dominate:** Assisted falls outnumber unassisted falls in 5 of the 6 quarters, and tie in the other (2024 Q1, 3 each). Because staff are present for assisted falls, this suggests staff handling and mobility-assistance practices are an area to review.
- **Unit B carries most of the falls:** Unit B accounts for **35 of the 48 falls** at Hospital 1 (about 73%), supporting the choice to launch the program there.

## Recommendations

1. Use **about 6 falls per quarter** as the baseline target to beat once the program launches.
2. Track the **assisted fall** rate separately, since it is the largest share and the most directly tied to staff practices and training.
3. Refresh the PivotTable each quarter (right-click, **Refresh**) after adding new falls to `FallsData`, and compare against this baseline.

## Assumptions & Limitations

- The data is **synthetic** and created for portfolio purposes.
- The report counts **number of falls**, not a rate. Falls per 1,000 patient days would be a fairer measure but needs patient-day data.
- The baseline covers one unit over six quarters, a small sample, so a quarter-to-quarter change of one or two falls may not be meaningful.
- Fall severity, time of day, and patient details are not in the dataset.

## Skills Demonstrated

- Excel Tables
- PivotTables (filters, rows, columns, values)
- Grouping dates by years and quarters
- Scoping an analysis to a business request
- Turning results into findings and recommendations

## Repository Contents

- `HC_Excel_Portfolio_Scenarios.xlsx`: the workbook (Scenario 1 uses the `Scenario 1 - Falls` and `S1 - Pivot` sheets)
- `README.md`: this file
- `images/`: screenshots of the PivotTable 

## Author - Diane Gordon

This project is part of my data analytics portfolio, showcasing Excel skills for healthcare analyst roles.

- **LinkedIn**: (https://www.linkedin.com/in/diagordon/)
- **GitHub**: (https://github.com/secretlyblu?tab=repositories)
