# 📊 RateMyProfessor Gender Bias Analysis  
**Author:** Kim Jin  
**Project Type:** Group Project (Lead Analyst for Gender Bias Analysis)  
**Date:** Dec. 2024  

---

## Project Overview  
This project investigates **potential gender bias in student evaluations of professors** using **RateMyProfessor (RMP) data**. Prior research suggests that male professors may receive **higher ratings** due to bias, but concerns about **sample size, confounders (e.g., teaching experience), and statistical rigor** make the evidence questionable.  

My role in this project focused on:  
1. **Examining gender bias in average ratings** (Are male professors rated higher?)  
2. **Analyzing gender differences in rating dispersion** (Do ratings for male/female professors vary differently?)  
3. **Estimating effect sizes** for these biases with **95% confidence intervals**.  

The dataset contains **student evaluations from RateMyProfessor**, including **professor ratings, difficulty levels, number of reviews, and demographic information**.

---

## Dataset & Preprocessing  
- **Data Source:** Publicly available RateMyProfessor dataset.  
- **Preprocessing Steps:**  
  - Removed professors with **fewer than 5 reviews** (to avoid unreliable ratings).  
  - Grouped professors into **4 rating count bins**: **(5–9, 10–14, 15–19, 20–24)** (controlling for experience).  
  - Filtered out ambiguous gender data (professors labeled both Male & Female).  
  - Standardized **categorical variables** and formatted numerical data for analysis.  

---

## Research Questions & Methods  

### **1️. Is There a Pro-Male Gender Bias in Average Ratings?**  
- **Statistical Test:** **Mann-Whitney U Test** (compares median ratings instead of means).  
- **Null Hypothesis:** No significant difference between **average ratings for male and female professors**.  
- **Findings:** No statistically significant gender bias was found in any rating group.  

### **2️. Do Male & Female Professors Have Different Rating Distributions?**  
- **Statistical Test:** **Kolmogorov-Smirnov (KS) Test** (compares distributions).  
- **Null Hypothesis:** No significant difference in **rating distribution spread** for male vs. female professors.  
- **Findings:** No statistically significant difference in rating variance between genders.  

### **3️. Estimating Effect Sizes (Bias & Dispersion Differences)**  
- **Metric for Bias in Ratings:** **Cohen’s d** (effect size measure for mean difference).  
- **Metric for Rating Dispersion:** **Standard Deviation Ratio** (female vs. male rating spread).  
- **Bootstrap Method:** Used to estimate **95% confidence intervals** for effect sizes.  
- **Findings:** Effect sizes were small, indicating **negligible practical significance**.  

---

## Results & Interpretation  
- Across **all rating bins**, **no strong evidence of gender bias** was found.  
- **Effect sizes were small**, suggesting any gender-related differences are **not practically meaningful**.  
- Results align with visualizations: when controllong for other factors, **male and female professors receive similar ratings and rating spreads**.  

---
