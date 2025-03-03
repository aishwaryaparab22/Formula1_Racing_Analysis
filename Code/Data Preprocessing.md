## Data Preprocessing

In this phase, we focused on merging and cleaning various datasets to create a comprehensive dataframe for analysis.

### Data Merging

We integrated multiple data sources through the following steps:

1. **Results DataFrame**: Merged secondary data from **races**, **results**, **drivers**, and **constructors** into a new dataframe called `results_df`.
2. **Qualifying DataFrame**: Created `qualifying_df` by merging `results_df` with qualifying data.
3. **Driver Standings**: The `driver_standings_df` combines race data, driver standings, and driver information for a complete view of driver performance.
4. **Constructor Standings**: Similarly, merged race data with constructor standings to create `constructor_standings_df`.
5. **Final Consolidation**: All relevant dataframes, including weather information and newly created dataframes, were merged into `final_df`, which contains 6,798 rows and 78 columns, covering the period from **1994 to 2023**.

   We also created binary dummy variables for driver's nationality, circuits, and constructors to facilitate statistical analysis.

### Data Cleaning

The data cleaning process involved removing **Null** values from the **Podium** column in `final_df`, along with unnecessary variables and fixing any irregularities. This ensures the dataset is clean, reliable, and ready for in-depth analysis.
