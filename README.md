Here is the complete, unified README.md file for your GitHub repository. It combines the project overview, methodology, repository structure, and the expanded requirements and setup instructions into a single, cohesive, copy-pasteable markdown file.README.mdMarkdown# 🎓 Impact of Behavioral and Academic Factors on CGPA

[![R-Language](https://img.shields.io/badge/Language-R-%23276DC3.svg?style=flat&logo=r&logoColor=white)](https://www.r-project.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[cite_start]This repository contains the dataset, R statistical scripts, and reporting assets for a predictive study analyzing the relationship between an undergraduate student's Cumulative Grade Point Average (CGPA) and various behavioral, cognitive, and academic predictors[cite: 3]. [cite_start]The analysis utilizes Multiple Linear Regression (MLR) to isolate the most critical drivers of academic success[cite: 104].

[cite_start]The complete comprehensive analysis and findings are documented in the accompanying file, **`report.docx`**[cite: 1].

---

## 📌 Project Overview

Understanding what drives academic success is critical for both students and educational institutions. [cite_start]This project analyzes survey data collected from **FAST University** undergraduate students to model how daily habits, engagement, and background academic performance impact a student's final CGPA[cite: 4].

### Variables Evaluated:
* [cite_start]🎯 **Dependent Variable ($Y$):** CGPA (Continuous numerical value)[cite: 3, 48].
* [cite_start]⚙️ **Independent Variables ($X$):** Weekly Study Hours, Focus Span (Minutes), Attendance Percentage, Procrastination Percentage, Leisure Hours, Class Participation Percentage, and Pre-University Grades (FSC/A-Level)[cite: 3, 45].

---

## 📊 Methodology & Analytical Framework

### 1. Data Collection & Sample
* [cite_start]**Target Population:** All undergraduate students at FAST University[cite: 40].
* [cite_start]**Sample Size:** $n = 43$ observations[cite: 43].
* [cite_start]**Sampling Frame:** Students from Section DS-D, Data Science (Batch 2022), ensuring a controlled academic environment and curriculum uniformity[cite: 43, 66].

### 2. Regression Modeling Process
[cite_start]The analysis follows a two-stage regression modeling approach using **R**[cite: 68]:
1. [cite_start]**Full Regression Model:** An initial linear regression model fitted against all collected numeric variables to capture broad variances[cite: 77].
2. [cite_start]**Feature Extraction (P-Value Selection):** Variables were filtered using their corresponding p-values[cite: 75, 81]. [cite_start]Predictors yielding a significance threshold close to or below $\alpha = 0.05$ were highlighted for optimized evaluation.
3. [cite_start]**Optimized Model Formulation:** A refined Multiple Linear Regression Model (MLRM) was constructed using the isolated predictors[cite: 88, 89].

#### Mathematical Form of the MLRM:
$$Y = \beta_0 + \beta_1x_1 + \beta_2x_2 + \beta_3x_3 + \epsilon$$

[cite_start]*Where $Y$ is the dependent variable (CGPA), $x_n$ represents the independent predictors, $\beta_n$ represents the coefficients, and $\epsilon$ is the residual error term[cite: 91, 93, 94, 96, 98].*

---

## 📈 Key Findings & Insights

* [cite_start]**Top Predictors Identified:** The refined analysis isolated **Class Participation Percentage**, **Attendance Percentage**, and **Procrastination Percentage** as critical determinants of academic variance[cite: 99].
* [cite_start]**Model Accuracy:** The final optimized regression model achieved an exceptional **Coefficient of Determination ($R^2 \approx 0.9793$)**, explaining approximately **97.93%** of the variance in student CGPAs[cite: 101].
* [cite_start]**Actionable Conclusion:** Regular class attendance and active classroom engagement show strong positive correlations with higher GPAs, while elevated procrastination tendencies inversely degrade academic scores[cite: 106, 109].

---

## 📂 Repository Structure

```text
├── data/
│   └── data_clean.csv        # Cleaned dataset containing survey responses
├── scripts/
│   └── cgp_analysis.R        # R script containing summary stats, plots, and regression code
├── plots/
│   ├── box_whisker_plot.png  # Distribution plot for all numeric variables
│   └── scatter_grid.png      # Scatter plot matrix showing multi-variable correlations
├── report.docx               # Full, comprehensive formal research report
└── README.md                 # Project executive summary (This file)
🛠️ Requirements & SetupTo replicate this analysis, generate the summary statistics, or reproduce the plots locally, follow the environment configuration and steps below.1. Prerequisites & EnvironmentR Environment: R (version 4.0.0 or higher recommended) or RStudio Desktop.Data File: Ensure data_clean.csv is placed inside the data/ directory relative to your working script.2. Install Required Package DependenciesThe script relies on ggplot2 for the box and scatter plots, and core utilities for statistical analysis. Open your R console or RStudio and run the following command to install the required libraries:R# Install required CRAN packages
install.packages(c("ggplot2", "GGally", "tidyverse"))
3. Step-by-Step ExecutionOption A: Running via Command Line / TerminalClone this repository to your local machine:Bashgit clone [https://github.com/yourusername/cgpa-factor-analysis.git](https://github.com/yourusername/cgpa-factor-analysis.git)
Navigate into the project directory:Bashcd cgpa-factor-analysis
Execute the R script directly:BashRscript scripts/cgp_analysis.R
Option B: Running via RStudio IDEOpen RStudio.Go to File -> New Project -> Existing Directory and select the cloned repository folder. This automatically sets your working directory to the project root.Open scripts/cgp_analysis.R.Run the script to execute the following pipeline (as detailed in report.docx):Summary Statistics: Outputs print(summary_stats) and print(modes) to the console.  Data Visualization: Generates and saves the Box and Whisker Plots and the Scatter Plot Grid.  Feature Selection: Fits the full model, extracts, and sorts the p-values via print(sorted_p_values).  Optimized MLRM: Fits the final model using the selected key tracking metrics to print the final $R^2$ value ($0.9793$) and target prediction results.  4. Expected Console OutputsUpon running the script successfully, your R console will display the formatted regression tables mirroring the steps in the report:Step 1: Full Model Summary (Residuals, Coefficients, Standard Error, t-values, and baseline F-statistic).  Step 2: A sorted array of p-values pinpointing the critical academic and behavioral metrics.  Step 3: The optimized Multiple Linear Regression Model metrics and the calculated $R^2$ validation output.  📜 ReferencesAll foundational academic frameworks, including studies on study hours (Plant et al., 2005), focus span (Becker et al., 2013), and attendance (Credé et al., 2010), are fully cited inside 
