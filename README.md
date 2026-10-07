# Weather Project
> The purpose of this project is to perform work using the data science methodology to determine whether it rains more in Seattle, WA or Pittsburgh, PA.
> For this project, I consider a city to be more rainy if it has precipitation on a greater number and proportion of days. Both cities are known for rainy weather, so I was genuinely curious to see which city has more rainy days based on the data.
---

## Project Overview

The goal of this project is to compare weather data from Seattle and Pittsburgh and compare precipitation

- **Objective:** Compare weather patterns in Seattle and Pittsburgh.
- **Domain:** Weather
- **Key Techniques:** Data cleaning, analysis, visualization, report

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** [Link to the data source(s) ](https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND)
- **Description:** Data from the weather in Pittsburgh and Data from the weather in Seattle. The data from this source includes precipitation, date, and location information needed for the analysis.

---

## Analysis

First, I needed to inspect the data from Seattle and Pittsburgh. I checked the columns in both datasets and made sure that I had date and precipitation columns. Then I compared the dataset sizes and checked if I had enough data for my analysis.

I converted the date column to datetime and checked for duplicates. Both datasets did not have duplicate dates. Then I saw that the Pittsburgh dataset did not have data before 11-04-2018, and the Seattle dataset was missing data from 11-04-2018 to 11-11-2018. This is why I decided to limit the date range from 11-11-2018 to 12-31-2022.

The next step was to join both datasets. In the new dataset, I had date, city, and precipitation columns. I started to inspect the newly created dataset. There were 205 missing precipitation values: 118 for Seattle and 87 for Pittsburgh. I used mean precipitation values to fill in the missing data.

After the dataset was clean, I saved it and started the analysis.

I decided to analyze mean daily precipitation, the number of days with precipitation, and the proportion of days with precipitation.


---

## Results

Based on my analysis, both Seattle, WA and Pittsburgh, PA are rainy cities, and I noticed that they are actually very similar.

The mean daily precipitation values are very close. Seattle has a mean daily precipitation of 0.1189 inches, while Pittsburgh has 0.1339 inches.

I decided to determine which city is rainier based on the number and proportion of days with precipitation. Seattle had more days with precipitation, with 846 days compared with 739 days in Pittsburgh.

The proportion of days with precipitation is significantly higher in Seattle in January, February, November, and December. It is significantly higher in Pittsburgh in July and August.

Based on the number and proportion of days with precipitation, I conclude that Seattle is rainier than Pittsburgh.

---

## Authors

- Your Name - [@Polina Dimitryuk](https://github.com/polinadimitryuk)

---

## Acknowledgements

- Tools/libraries used: pandas, numpy, matplotlib.pyplot, seaborn