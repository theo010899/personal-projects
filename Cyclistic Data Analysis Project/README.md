
# Cyclistic Bike-Share Analysis

## Introduction
This project analyzes Cyclistic (Divvy) bike-share trip data to answer a key business question from the Google Data Analytics Capstone case study:

**How do annual members and casual riders use Cyclistic bikes differently?**

The analysis follows the data analysis lifecycle:
- Ask
- Prepare
- Process
- Analyze
- Share
- Act

The goal is to identify behavioral differences between rider types and provide recommendations for converting casual riders into annual members.

## Table of Contents
1. Introduction
2. Business Task
3. Data Sources
4. Project Structure
5. Installation
6. Usage
7. Data Preparation
8. Analysis Performed
9. Key Findings
10. Contributors
11. License

## Business Task

Determine how annual members and casual riders use Cyclistic bikes differently and use those insights to support marketing strategies that increase annual memberships.

## Data Sources

### Case Study Documentation
- `Case Study 1_ How does a bike-share navigate speedy success.pdf`

### Trip Data
- Historical Cyclistic/Divvy trip data
- Data provider: Lyft Bikes and Scooters, LLC (Divvy)
- Source: https://divvy-tripdata.s3.amazonaws.com/index.html

## Project Structure

```text
.
├── cyclistics_analysis.ipynb/html
├── Case Study 1_ How does a bike-share navigate speedy success.pdf
├── *.zip (trip data files)
├── *.csv (data summary files)
└── casual_and_member_diffs powerpoint presentation
```

## Installation

### Requirements

Python 3.10+ recommended

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn
```

## Usage

1. Download Cyclistic/Divvy trip datasets.
2. Place CSV files in the project directory.
3. Open:

```bash
jupyter notebook cyclistics_analysis.ipynb
```

4. Run all notebook cells.

The notebook:
- Loads and combines CSV files.
- Cleans and transforms data.
- Creates summary statistics.
- Generates visualizations.
- Exports aggregated results.

## Data Preparation

The notebook performs the following preprocessing steps:

### Data Cleaning
- Converts `started_at` and `ended_at` to datetime.
- Removes rows containing missing values.
- Sorts rides by start time.
- Removes rides with negative durations.
- Converts IDs and station fields to string types.

### Feature Engineering
Creates:

- `member_type`
- `Trip_length [secs]`
- `date`
- `month`
- `day`
- `year`
- `day_of_week`

### Data Reduction
Drops unnecessary coordinate columns:

- `start_lat`
- `start_lng`
- `end_lat`
- `end_lng`

## Analysis Performed

### Descriptive Statistics
- Ride duration distribution
- Mean, median, min, and max ride duration
- Member vs casual comparisons

### Behavioral Analysis
- Average ride length by weekday
- Ride counts by weekday
- Ride counts by rider type
- Ride duration by rider type
- Rideable type usage patterns

### Station Analysis
- Most frequently used start stations
- Most frequently used end stations

### Visualizations
- Ride count vs weekday
- Average ride duration vs weekday
- Rideable type vs ride count
- Rideable type vs average ride duration

## Key Findings

### Casual Riders
- Ride primarily for leisure and recreation.
- Activity increases significantly toward weekends.
- Frequently start and end trips near recreational destinations and tourist attractions.
- Average ride duration is substantially longer than member rides.

### Annual Members
- Display strong weekday commuting patterns.
- Ride counts peak during the work week.
- Commonly use stations near business districts and transit hubs.
- Take shorter but more frequent trips.

### Bike Type Preferences
- Casual riders show strong usage of electric bikes.
- Members use both bike types heavily, with stronger classic-bike usage.
- Casual riders generally keep bikes longer regardless of bike type.


## Dependencies

- numpy
- pandas
- matplotlib
- seaborn
- glob (standard library)

## Contributors

- Theodore Chidi-Maha (analysis author)

## License

This project uses publicly available Divvy/Cyclistic trip data subject to the provider's licensing terms.

Please review the original data license before redistribution.
