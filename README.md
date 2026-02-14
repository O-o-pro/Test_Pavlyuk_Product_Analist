# Mobile Product Analytics Case Study

This repository contains two analytical case studies simulating real-world mobile subscription product analytics tasks:

1. A/B Pricing Experiment
2. 52-Week LTV Forecasting Model

The analyses focus on business impact, statistical rigor, and decision-making support.

---

# Case 1 — A/B Test: Pricing Experiment

## Objective

Evaluate the impact of a new pricing model on conversion and monetization metrics.

## Business Context

The company tested a new subscription pricing structure.  
Goal: Increase revenue without harming funnel performance.

---

## Experiment Validation

- ~50/50 traffic split between control and treatment
- Country-level distribution checked
- 7-day experiment duration
- Revenue tracked for first 30 days

---

## Metrics

Primary Metric:
- Paid Conversion Rate

Secondary Metrics:
- Trial Conversion Rate
- Revenue per Install (RPI)

---

## Statistical Methods

- Z-test for proportions
- Wilson confidence intervals
- Bootstrap uplift estimation (5,000 resamples)

This ensures robustness beyond classical parametric testing.

---

## Key Findings

- Trial conversion decreased
- Paid conversion increased
- Revenue per Install increased
- Paid CR uplift statistically significant
- Bootstrap CI confirmed positive uplift

---

## Business Recommendation

Roll out new pricing to 100% traffic with continued monitoring of:

- Retention
- LTV
- Country-level performance

---

# Case 2 — 52-Week LTV Forecast

## Objective

Forecast full-year cumulative LTV based on 32 weeks of observed cohort data.

Used for:
- CAC threshold definition
- Marketing budget planning
- Revenue forecasting

---

## Data Processing

- Cohort-based aggregation
- Cumulative revenue per user
- Weighted average across cohorts

---

## Modeling Approach

Two non-linear models were tested:

1. Exponential saturation model  
   LTV(t) = a * (1 - exp(-b * t))

2. Logarithmic growth model  
   LTV(t) = a * log(1 + b * t)

---

## Model Evaluation

- Manual R² calculation
- MAPE
- Out-of-sample validation (Train: weeks 1–24, Test: 25–32)
- Residual diagnostics
- Bootstrap confidence intervals (1,000 resamples)

This ensures both in-sample fit and generalization ability.

---

## Final 52-Week Forecast

Base scenario: mean bootstrap estimate  
Conservative: 5th percentile  
Optimistic: 95th percentile  

Revenue forecast calculated for 100,000 new users.

---

## Business Impact

The model provides:

- Data-driven CAC ceiling
- Scenario-based revenue planning
- Risk-aware marketing allocation

---

# Tools Used

- Python
- Pandas
- NumPy
- SciPy
- Statsmodels
- Matplotlib

---

# Author

Product Analytics Case Study  
Prepared for mobile subscription product environment
