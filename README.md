# NYC Restaurant Inspection Analysis

Which restaurants are most likely to score worse than an A on NYC health inspections?

## Summary
The analysis involved almost 292K violation records from the NYC Department of Health, which was converted into 82,859 inspections with an emphasis on 46,830 routine initial inspections. Cuisine was much more related to failure than the borough: the range of not-A rates was between 18% to 63% in various cuisines compared to 6 points in different boroughs.

## Approach
1. Cleaned the data (duplicates, text dates, placeholder rows, invalid boroughs)
2. Converted violation-level rows into one row per inspection
3. Kept only routine initial inspections so the comparison is fair
4. Defined failing as a score of 14+ (not an A), with 28+ as a stricter check
5. Compared failure rates by borough, cuisine, and year, and checked that the cuisine pattern wasn't just a borough effect

## Key findings
- Highest not-A rates: Indian, Thai, Asian/Asian Fusion
- Lowest: Donuts, Salads, Hamburgers
- Failure rates rose modestly from 2022 to 2026

## Limitations
Associations only, not causes. Restaurant age, size, and chain status are not controlled for. See the notebook for details.

## How to run
1. Download the data: search "DOHMH New York City Restaurant Inspection Results" on NYC Open Data and export as CSV
2. Save it in a `data/` folder
3. `pip install pandas matplotlib seaborn`
4. Open `analysis.ipynb` and run all cells

Note: update the filename in the notebook's `read_csv` line to match your download.

## Tools
Python, pandas, matplotlib, seaborn
