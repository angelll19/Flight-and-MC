# Random Walk & Flight Analysis (2000–2004)

This project contains two main parts:

1. A Metropolis-Hastings random walk simulation using the Laplace distribution
2. A flight analysis project using Harvard Dataverse data from 2000 to 2004

The project was implemented in both **R and Python**, with functions used to automate data reading, cleaning, analysis, and visualization.

---

## Overview

This coursework combines statistical simulation and real-world flight data analysis. The first part uses the Metropolis-Hastings algorithm to generate random samples and study convergence. The second part analyzes airline delays, plane age effects, and flight diversion patterns using historical flight data from 2000 to 2004. :contentReference[oaicite:3]{index=3} :contentReference[oaicite:4]{index=4}

---

## Part 1: Metropolis-Hastings Random Walk

The first section implements a Metropolis-Hastings algorithm to generate samples from a target Laplace distribution. Random numbers are proposed from a normal distribution and accepted or rejected based on the Metropolis rule.

### Main tasks
- Define the target distribution
- Generate random samples using Markov Chain Monte Carlo
- Compare the generated samples with the true distribution
- Evaluate convergence using R-hat values
- Test different step sizes to identify a suitable sampling range

### Key outputs
- Histogram and kernel density plots
- Distribution comparison between estimated and actual curves
- R-hat convergence diagnostics
- Sample mean and standard deviation estimates

The report shows that the generated samples approximate the target distribution well, and that smaller step sizes can slow convergence while larger step sizes improve stability after a point. :contentReference[oaicite:5]{index=5} :contentReference[oaicite:6]{index=6}

---

## Part 2: Flight Delay Analysis (2000–2004)

This section uses flight data from Harvard Dataverse covering five years, 2000 to 2004. The data was read from CSV files and automated using functions in both R and Python. Delay was defined as a flight arriving or departing 15 minutes or more late, and departure delay and arrival delay were analyzed separately to avoid double counting. :contentReference[oaicite:7]{index=7}

### Objectives
- Identify the best day of the week to fly
- Identify the best time of day to avoid delays
- Examine whether older planes suffer more delays
- Analyze flight diversion patterns

### Data preparation
- Combined data from 2000 to 2004
- Filtered out cancelled and diverted flights where needed
- Selected only the relevant variables for each analysis
- Created delay ratio variables
- Converted year and time-related fields for analysis
- Merged flight data with plane data for age analysis

---

## Key Findings

### Best day to fly
Saturday was found to be the best day overall because it consistently had the lowest delay ratio and low average delay. Friday showed the highest delay risk and should be avoided.

### Best time to fly
The 4:00–8:00 time window was the best overall for minimizing delay risk. Although 0:00–4:00 sometimes had lower average delay, 4:00–8:00 had a lower probability of delay and was more consistent across the five-year period. Late afternoon and evening flights, especially 16:00–20:00, had higher delay rates. 
### Plane age and delays
The analysis found no strong evidence that older planes suffer more delays. The relationship between plane age and delay was weak, with low correlation and almost no linear relationship.

### Diversion prediction
A logistic regression model was used to predict diverted flights. Features such as day of month, carrier, departure time, and distance showed some influence, but the model was affected by class imbalance. The model achieved an AUC of around 0.64, which is only slightly better than random guessing.

---

## Tools Used

- R
- Python

---

## Dataset

The flight analysis uses Harvard Dataverse flight data from **2000 to 2004**. The report also uses plane-data.csv for the aircraft age analysis. 

The complete dataset, along with supplementary information and variable descriptions, can be downloaded from the Harvard Dataverse at https://doi.org/10.7910/DVN/HG7NV7

---

## How to Run

### Prerequisites
- R
- Python
- Required packages for data analysis and visualization

### Steps
1. Clone the repository
2. Open the R or Python scripts / notebook files
3. Run the simulation and analysis sections
4. Review the generated plots and results

---

## Summary

This project demonstrates both statistical theory and practical data analysis. It combines simulation, delay analysis, plane-age investigation, and logistic regression to study airline performance across multiple years.

The main takeaway is that delay patterns depend more on day and time than on plane age, and that Saturday and 4:00–8:00 are the most favorable choices for minimizing delay risk. 
