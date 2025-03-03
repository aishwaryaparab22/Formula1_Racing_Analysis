# Data Directory Overview

This directory contains all datasets used in the analysis of the Formula 1 project. The datasets are categorized into three main folders: `raw_data` and `processed_data`.

## Data Sources
All datasets originate from reliable platforms, including:
- [Formula 1 Official Website](https://www.formula1.com)
- [Ergast API](https://ergast.com/mrd/)
- [Kaggle Formula 1 Dataset](https://www.kaggle.com/rohanrao/formula-1-world-championship-1950-2020)

Ensure to adhere to the licensing agreements and provide attribution as necessary when using these datasets.

## Directory Structure

### 1. **raw_data/**
This folder contains original datasets sourced from various platforms. Each file represents a different aspect of Formula 1 statistics.

- **circuits.csv**: Contains information about the race circuits used in Formula 1, including their names, locations, and characteristics.
- **constructor_results.csv**: Provides results for constructors in individual races, detailing their performance.
- **constructor_standings.csv**: Displays the standings of constructors over a season, based on points earned.
- **constructors.csv**: Contains information about constructors, including their names, IDs, and nationality.
- **driver_standings.csv**: Shows the standings of drivers over a season, based on points earned.
- **drivers.csv**: Includes detailed information about drivers, such as names, IDs, and birthdates.
- **qualifying.csv**: Contains qualifying session results for each race, detailing drivers' positions and times.
- **races.csv**: Provides detailed information about each race, including the race name, date, and circuit.
- **results.csv**: Contains the final results of each race, including driver positions, laps completed, and time taken.
- **status.csv**: Provides details on the status of drivers during races, indicating whether they finished, retired, or were disqualified.
- **overtakes.csv**: Contains data on overtakes made by each driver, useful for performance metrics.
- **casualty_data.csv**: Includes casualty data for analyzing the safety aspects of racing.

### 2. **processed_data/**
This folder contains cleaned and processed datasets ready for analysis. These files have undergone data cleaning, merging, and transformation to ensure quality and usability.

- **final_df.csv**: The final merged dataset used for modeling and analysis.
