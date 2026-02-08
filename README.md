# Predicting Parkinson’s Disease Severity from Voice Acoustics

This repository contains an end-to-end statistical analysis and modeling project focused on predicting Parkinson’s disease severity using longitudinal voice-acoustic data. The project applies linear mixed-effects modeling to account for repeated measurements and subject-level heterogeneity, enabling more reliable inference compared to standard regression approaches.

---

## 📌 Project Overview

Parkinson’s disease is a progressive neurological disorder where symptom severity varies substantially across individuals and over time. Traditional regression models often fail to account for the longitudinal structure of clinical monitoring data, leading to biased estimates and loss of statistical power.

In this project, we analyze a large telemonitoring dataset of voice recordings from Parkinson’s patients and develop a **linear mixed-effects model (LMM)** to predict disease severity while properly handling repeated measurements per subject.

---

## 📊 Dataset

- **Source:** UCI Machine Learning Repository  
- **Dataset:** Oxford Parkinson’s Disease Telemonitoring Dataset  
- **Observations:** 5,875 voice recordings  
- **Subjects:** 42 patients  
- **Response Variable:**  
  - `total_UPDRS` — Unified Parkinson’s Disease Rating Scale (clinical severity score)
- **Predictors:**  
  - Demographics: Age, Sex  
  - Acoustic features: Jitter, Shimmer, RPDE, DFA, PPE, and related voice measures

The dataset was originally collected to study the feasibility of non-invasive, remote monitoring of Parkinson’s disease progression.

---

## 🔍 Methodology

### 1. Exploratory Data Analysis (EDA)
- Distributional analysis of disease severity
- Visualization of demographic effects (age and sex)
- Assessment of longitudinal structure and repeated measurements

### 2. Multicollinearity Diagnosis
- Correlation matrix analysis
- Variance Inflation Factor (VIF) analysis
- Feature reduction to retain representative acoustic measures and ensure stable coefficient estimation

### 3. Baseline Modeling (OLS)
- Ordinary Least Squares regression on subject-aggregated data
- Identification of loss in statistical power due to aggregation
- Motivation for adopting a mixed-effects framework

### 4. Linear Mixed-Effects Modeling
- Random intercept model with subject-specific effects
- Full use of longitudinal data without violating independence assumptions
- Comparison against OLS results

### 5. Model Evaluation
- Residual diagnostics (normality, homoscedasticity)
- Intraclass Correlation Coefficient (ICC) estimation
- Model comparison between OLS and LMM

---

## ✅ Key Results

- Aggregating repeated measurements severely reduced statistical power and masked meaningful effects.
- Linear mixed-effects modeling substantially improved inference by accounting for subject-level variability.
- Age emerged as a significant biological predictor of disease severity.
- Voice-acoustic features contributed complementary information once multicollinearity was controlled.
- ICC analysis confirmed strong within-subject correlation, justifying the mixed-effects approach.

---

## 🧠 Why Mixed-Effects Models?

This project demonstrates why mixed-effects models are essential for:
- Longitudinal healthcare data
- Repeated measurements per subject
- Clinical monitoring and telemedicine applications
- Reliable biomarker identification

---

## 📁 Repository Structure

