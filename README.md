# Effect of Key Events on COVID-19 new cases in Quebec: A Regression Analysis

### Collaborators:

- [Mark Owen](https://github.com/take1step)
- [Ivan Stefanov](https://github.com/vanko2011)

### Introduction

This project aims to estimate the effect of three significant events related to COVID-19 in Quebec, Canada, using regression analysis. The events considered are:

- The 20/3/2020 lockdown
- The reopening of schools on 31/8/2020
- The 25/12/2020 lockdown
  
For each event, we collected data on COVID-19 measures, such as cases, hospitalizations, or deaths, to analyze their impact on the pandemic's trajectory. The primary goal is to determine whether these events had a statistically significant effect on COVID-19 new cases.

### Data Collection and Analysis

We used RDD (Regression Discontinuity Design) to analyze the effect of the events on COVID-19 new cases. RDD is a quasi-experimental design that allows us to estimate causal effects by leveraging the sharp changes (discontinuities) that occur at the event dates. We collected relevant COVID-19 data from "DONNÉES QUÉBEC." [COVID-19: Portrait quotidien des cas confirmés, Gouvernement du Québec, 2023](https://www.donneesquebec.ca/recherche/dataset/covid-19-portrait-quotidien-des-cas-confirmes).

### Regression Design

For each event, we designed a regression model to estimate the effect on COVID-19 new cases. Some of the considerations in our regression design were:

- Cutoff Parameter: The event date served as the cutoff point, and we analyzed the effect of the measure taken both before and after the event.
- Time Frame: We carefully selected the amount of time included on both sides of the cutoff to capture the impact of the events effectively. The time frame selected was 60 days. Longer time frames were considered when it was relevant for the analysis.
- Polynomial Degree: We experimented with different polynomial degrees to account for potential non-linear relationships between the events and COVID-19 measures. We selected the appropriate degree (degree of 1) based on goodness-of-fit and interpretability.

### Findings

We obtained statistically significant results for all three events, indicating that they had a discernible impact on COVID-19 new cases in Quebec. Our analysis revealed the following key findings:

- The 20/3/2020 Lockdown: The graphs and results suggest that the first lockdown implemented by the government of Quebec on 20/3/2020 had a minimal impact on the number of new cases. It seems that on the short term, the lockdown was able to slow down the spread of the virus and after the first 30 days post lockdown period, we already started seeing a drop of new daily covid cases in the province of Quebec.

  ![rdd-1](https://github.com/felipegomez30/covid-regression-project/assets/130583163/d3fab758-1ebe-4397-91bd-d654f665fac5)

- The reopening of schools on 31/8/2020: Using RDD to model the data shows a significant correlation between the reopening of schools during and a subsequent sharp increase in cases. This suggests that reopening schools may have contributed to the spread of the virus. However, other factors, such as community transmission rates, variants, vaccine coverage gaps, adherence to safety measures within schools, could also have played a role in the observed increase in cases.

  ![rdd-2](https://github.com/felipegomez30/covid-regression-project/assets/130583163/0896d02f-ea7f-42da-b7c5-8a1c902fac83)

- The 25/12/2020 Lockdown: The findings suggest that the Christmas lockdown implemented by the government of Quebec on December 25th, 2020, had a significant impact on the number of new cases.

![rdd-3](https://github.com/felipegomez30/covid-regression-project/assets/130583163/f8770b06-9ced-46ff-905b-5cfca37989d8)

### Conclusion

The regression analysis using RDD provided valuable insights into the impact of key events on COVID-19 new cases in Quebec. Understanding the effects of such events can help policymakers and health authorities make informed decisions and implement targeted measures to control the pandemic effectively.

Note: We have included the [Jupyter Notebook](https://github.com/felipegomez30/covid-regression-project/blob/main/notebook/COVID-regression-model.ipynb) containing the code, detailed analysis, and visualization of the results in this repository. Feel free to explore the notebook to delve deeper into our findings.
