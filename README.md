# Prognostic Role of Peritumoral CXC Motif Chemokine Ligand 17 (CXCL17) in Hepatocellular Carcinoma (HCC)

## Project Overview

This repository contains the statistical analysis code for BIOST 713 Project 2, investigating the association between peritumoral CXC motif chemokine ligand 17 (CXCL17) expression and overall survival (OS) in patients with hepatocellular carcinoma (HCC). The analysis follows a pre-specified Statistical Analysis Plan (SAP) and includes multivariable Cox proportional hazards regression, diagnostic testing, and adjusted survival visualization.

## Study Objectives

### Primary Aim (Aim 1)
Assess the independent association between continuous peritumoral CXC motif chemokine ligand 17 (CXCL17P) expression and overall survival (OS) after adjusting for clinical confounders including:
- Tumor multiplicity
- Alpha-fetoprotein (AFP) levels
- Aspartate aminotransferase (AST) levels  
- Tumor size
- Vascular invasion
- Tumor-Node-Metastasis (TNM) stage
- Barcelona Clinic Liver Cancer (BCLC) stage

### Secondary Aim (Aim 2)
Describe baseline characteristics of the study population and univariate associations with overall survival (OS).

### Exploratory Aim (Aim 3)
Visualize adjusted survival experience for patients with high (75th percentile) vs low (25th percentile) peritumoral CXC motif chemokine ligand 17 (CXCL17P) expression.

## Data Source

The analysis uses the `hepatoCellular` dataset from the `asaur` R package, containing clinical and pathological data from hepatocellular carcinoma (HCC) patients who underwent curative surgical resection.

## Key Statistical Methods

- **Primary Analysis**: Multivariable Cox proportional hazards regression
- **Contrast Analysis**: Comparison of 75th vs 25th percentile of peritumoral CXC motif chemokine ligand 17 (CXCL17P) expression
- **Descriptive Statistics**: Table 1 with baseline characteristics
- **Univariate Analysis**: Separate Cox models for each covariate
- **Diagnostic Testing**:
  - Proportional hazards (PH) assumption (Schoenfeld residuals)
  - Linearity assumption (Martingale residuals)
  - Influential observations (DFBETAS)

## File Structure
├── README.md # This file
├── 713_project2.Rmd # Main R Markdown analysis file

## Analysis Workflow

1. **Data Preparation**
   - Load required libraries (tidyverse, survival, survminer, gtsummary, etc.)
   - Create complete-case analysis dataset
   - Convert categorical variables to factors with descriptive labels

2. **Descriptive Statistics (Aim 2)**
   - Generate Table 1: Baseline characteristics
   - Run univariate Cox models for all covariates

3. **Primary Analysis (Aim 1)**
   - Fit multivariable Cox model
   - Calculate contrast (75th vs 25th percentile of peritumoral CXC motif chemokine ligand 17 (CXCL17P))
   - Generate Table 2: Multivariable model results
   - Generate Table 3: Contrast results

4. **Diagnostic Testing**
   - Test proportional hazards (PH) assumption (Figure 2)
   - Test linearity assumption (Figure 3)
   - Identify influential observations (Figure 4)

5. **Adjusted Survival Curves (Aim 3)**
   - Generate Figure 1: Adjusted survival curves by peritumoral CXC motif chemokine ligand 17 (CXCL17P) expression level

## Key Results Output

The analysis produces:
- **Table 1**: Baseline characteristics of hepatocellular carcinoma (HCC) patients
- **Table 2**: Multivariable Cox model results with hazard ratio (HR), 95% confidence interval (CI), and p-values
- **Table 3**: Contrast results (75th vs 25th percentile of peritumoral CXC motif chemokine ligand 17 (CXCL17P))
- **Figure 1**: Adjusted survival curves for high vs low peritumoral CXC motif chemokine ligand 17 (CXCL17P) expression
- **Figure 2**: Schoenfeld residual plots for proportional hazards (PH) assumption testing
- **Figure 3**: Martingale residual plot for linearity testing
- **Figure 4**: DFBETAS plot for influential observations

## Statistical Significance

- Two-sided α = 0.05 defines statistical significance
- Hazard ratios (HR) reported with 95% confidence intervals (CI)
- Complete-case analysis with non-informative missingness assumption

## Software Requirements

```r
# Required R packages
library(tidyverse)
library(survival)
library(survminer)
library(gtsummary)
library(broom)
library(broom.helpers)
library(gridExtra)
library(doBy)
library(multcomp)
library(gt)
