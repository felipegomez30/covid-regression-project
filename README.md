# Effect of Key Events on COVID-19 new cases in Quebec: A Regression Analysis

### Introduction

This project aims to estimate the effect of three significant events related to COVID-19 in Quebec, Canada, using regression analysis. The events considered are:

- The 20/3/2020 lockdown
- The reopening of schools on 31/8/2020
- The 25/12/2020 lockdown
  
For each event, we collected data on COVID-19 measures, such as cases, hospitalizations, or deaths, to analyze their impact on the pandemic's trajectory. The primary goal is to determine whether these events had a statistically significant effect on COVID-19 new cases.

### Data Collection and Analysis

We used RDD (Regression Discontinuity Design) to analyze the effect of the events on COVID-19 new cases. RDD is a quasi-experimental design that allows us to estimate causal effects by leveraging the sharp changes (discontinuities) that occur at the event dates. We collected relevant COVID-19 data from "DONNÉES QUÉBEC." [COVID-19: Portrait quotidien des cas confirmés, Gouvernement du Québec, 2023](https://www.donneesquebec.ca/recherche/dataset/covid-19-portrait-quotidien-des-cas-confirmes).

### Regression Design

For each event, we designed a regression model to estimate the effect on COVID-19 measures. Some of the considerations in our regression design were:

- Cutoff Parameter: The event date served as the cutoff point, and we analyzed the effect of the measure taken both before and after the event.
- Time Frame: We carefully selected the amount of time included on both sides of the cutoff to capture the impact of the events effectively. The time frame selected was 60 days. Longer time frames were considered when it was relevant for the analysis.
- Polynomial Degree: We experimented with different polynomial degrees to account for potential non-linear relationships between the events and COVID-19 measures. We selected the appropriate degree (degree of 1) based on goodness-of-fit and interpretability.

### Findings

We obtained statistically significant results for all three events, indicating that they had a discernible impact on COVID-19 measures in Quebec. Our analysis revealed the following key findings:

- 20/3/2020 Lockdown: The lockdown implementation resulted in a significant reduction in COVID-19 cases and hospitalizations, indicating its effectiveness in controlling the spread of the virus.

  ![rdd-1](https://github.com/felipegomez30/covid-regression-project/assets/130583163/d3fab758-1ebe-4397-91bd-d654f665fac5)

- 31/8/2020 School Reopening: The reopening of schools led to a notable increase in COVID-19 cases, suggesting that it contributed to the rise in infections during that period.

  ![rdd-2](https://github.com/felipegomez30/covid-regression-project/assets/130583163/0896d02f-ea7f-42da-b7c5-8a1c902fac83)

- 25/12/2020 Lockdown: The second lockdown implemented on Christmas Day had a significant effect in curbing the spread of COVID-19, leading to a decline in cases, hospitalizations, and deaths.

![rdd-3](https://github.com/felipegomez30/covid-regression-project/assets/130583163/f8770b06-9ced-46ff-905b-5cfca37989d8)

### Conclusion

The regression analysis using RDD provided valuable insights into the impact of key events on COVID-19 measures in Quebec. Understanding the effects of such events can help policymakers and health authorities make informed decisions and implement targeted measures to control the pandemic effectively.

Note: We have included the Jupyter Notebook containing the code, detailed analysis, and visualization of the results in this repository. Feel free to explore the notebook to delve deeper into our findings.
