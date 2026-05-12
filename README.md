# Prognostic Role of Peritumoral CXCL17 in Hepatocellular Carcinoma

## Project Overview

This repository contains the statistical analysis code for BIOST 713 Project 2, investigating the association between peritumoral CXCL17 expression and overall survival in patients with hepatocellular carcinoma (HCC). The analysis follows a pre-specified Statistical Analysis Plan (SAP) and includes multivariable Cox proportional hazards regression, diagnostic testing, and adjusted survival visualization.

## Study Objectives

### Primary Aim (Aim 1)
Assess the independent association between continuous peritumoral CXCL17 expression (CXCL17P) and overall survival after adjusting for clinical confounders including:
- Tumor multiplicity
- AFP levels
- AST levels  
- Tumor size
- Vascular invasion
- TNM stage
- BCLC stage

### Secondary Aim (Aim 2)
Describe baseline characteristics of the study population and univariate associations with overall survival.

### Exploratory Aim (Aim 3)
Visualize adjusted survival experience for patients with high (75th percentile) vs low (25th percentile) CXCL17P expression.

## Data Source

The analysis uses the `hepatoCellular` dataset from the `asaur` R package, containing clinical and pathological data from HCC patients who underwent curative surgical resection.

## Key Statistical Methods

- **Primary Analysis**: Multivariable Cox proportional hazards regression
- **Contrast Analysis**: Comparison of 75th vs 25th percentile of CXCL17P expression
- **Descriptive Statistics**: Table 1 with baseline characteristics
- **Univariate Analysis**: Separate Cox models for each covariate
- **Diagnostic Testing**:
  - Proportional hazards assumption (Schoenfeld residuals)
  - Linearity assumption (Martingale residuals)
  - Influential observations (DFBETAS)

## File Structure
