# fitbit-fitness-data-visualization
This project explores relationships between physical activity, sleep, and energy expenditure using Fitbit fitness tracker data (April–May 2016, from Kaggle). Conducted data preprocessing, visualization, correlation analysis, and statistical testing using Python, Pandas, Matplotlib, Seaborn, and SciPy to derive actionable health insights.

## Table of Contents
1. [Data Description](#data-description)
2. [Analysis Tasks](#analysis-tasks)
3. [Requirements](#requirements)
4. [How to Run](#how-to-run)
5. [Results](#results)

## Data Description
The CSV files used for data analysis in this project are a part of the Kaggle's FitBit Fitness Tracker Data.

## Analysis Tasks
### 1. Exploratory Analysis by User
- **Heart Rate**: Downsampled to 12-hour intervals and visualized for 5 semi-random users.
- **Sleep Duration**: Hours asleep over time plotted for the same 5 users.
- **Daily Steps**: Daily step counts visualized for the same users.
- **Weight Change**: Weight over time plotted for the user with the most records.

### 2. Data Merging and Processing
- **Hourly Data**: Merged steps, intensity, and calories datasets.
- **Minutely Data**: Merged calories, intensity, and MET datasets.
- **Date Conversion**: All time columns converted to datetime for consistency.
- **Heart Rate**: Processed average heart rate per minute and merged with minutely data.

### 3. Visualization and Relationships
- Scatterplots and line plots show relationships between:
  - Steps vs Calories
  - Intensity vs Calories
  - Time in Bed vs Minutes Asleep
  - Sedentary Minutes vs Minutes Asleep
- Distribution of activity intensity over a day per user (for 5 semi-randomly selected users).

### 4. Statistical Analysis
- **Significant Differences in Calories**: Compared calories burned between highly active and less active users using a t-test.
- **Least Significant Difference**: Compared calories burned on Monday vs Tuesday using a t-test.

## Requirements
**Python Version:** 3.8+  
**Libraries Used:**
```bash
pip install pandas numpy matplotlib plotnine scipy
```

## How to Run
1. Place all Fitabase CSV datasets in a fitabase-data folder.
2. Open the Fitabase_Analysis.ipynb Jupyter Notebook.
3. The seed for the semi-randomly selected users may be updated for true randomness; the fixed random seed was utilized for reproducibility.
5. Run the notebook cells sequentially.

## Results
- There is a strong positive correlation between step count and calories
- There is a strong positive correlation between time in bed and minutes asleep
- There is a negative relationship between sedentary time and total sleep duration
- Statistical testing found that calories significantly differs between highly active and less active users
- Statistical testing also found that calories do not vary meaningfully between different days of the week
  
From the results, an understanding of correlation is created; however, no conclusion about causation was made. Overall, the results emphasize the importance of consistent, active behavior in promoting energy balance and healthy sleep patterns. These insights illustrate how data-driven analyses of wearable data can be applied to monitor personal well-being and develop recommendations.

## References
[FitBit Fitness Tracker Data (Kaggle)](https://www.kaggle.com/datasets/arashnic/fitbit/data)
