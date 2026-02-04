# Wearable Data Analysis  
**Behavioral Patterns and Energy Expenditure from Fitbit Data**

**View the full analysis:**  
[Rendered analysis notebook (HTML)](results/Wearable-data-analysis.html)

---
## Project Overview

This project analyzes daily activity data from a Fitbit wearable to explore how **behavioral patterns** and **energy expenditure** vary across weekdays and weekends.

The emphasis is on **interpretable, physiologically grounded analysis**, avoiding misleading aggregation or ratio-based artifacts that commonly appear in wearable data summaries.

All visualizations are performed at the **single-user level** to preserve behavioral clarity.

---

## Key Questions

1. **Behavioral structure**  
   Do step count patterns differ between weekdays and weekends?

2. **Energy context**  
   How does total energy expenditure relate to movement volume?

3. **Methodological insight**  
   What are the limitations of ratio-based wearable metrics such as calories per step?

---

## Key Findings

- **Behavioral variability:**  
  Weekday step counts were more consistent, while weekends exhibited greater variability, suggesting differences in routine-driven activity patterns.

- **Energy expenditure context:**  
  Calories increased with step count as expected; however, ratio-based metrics revealed important interpretive limitations when baseline energy expenditure is not separated from movement volume.

- **Methodological insight:**  
  Calories per step decreases as daily step count increases because total daily energy expenditure includes baseline metabolic processes (e.g., BMR and non-locomotor activity). As movement volume increases, this fixed baseline is distributed across more steps.  
  This highlights why behavioral volume (steps) and physiological cost should be interpreted separately in wearable data analysis.

---

## Repository Structure
<pre>
wearable-data-analysis/
├── data/
│   └── dailyActivity_merged.csv
├── scripts/
│   └── fitbit_activity_analysis.Rmd
├── results/
│   └── fitbit_activity_analysis.html
└── README.md
</pre>
---

## Tools & Methods

- **Language:** R  
- **Packages:** tidyverse, lubridate, ggplot2  
- **Approach:**
  - Feature engineering (weekday vs weekend)
  - Single-user visualization
  - Distributional and variability-based summaries
  - Conservative handling of ratio-based metrics

Weekly aggregation and normalization were intentionally de-emphasized to avoid misleading trends caused by partial weeks or baseline energy confounding.

---

## Why This Matters

This project demonstrates an approach to wearable data analysis that prioritizes:

- Scientific judgment over flashy visuals  
- Physiological context over naïve ratios  
- Clear communication of limitations and assumptions  

These principles align with best practices in applied human performance and health analytics.

---

## Author

**Mitchell Talton**  
B.S. Exercise Science   
Training in biomechanics, wearable data, and human performance analysis


