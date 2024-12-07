# Phase 3: Correlation and Regression Analysis Documentation

## Overview
Phase 3 investigates the relationship between electricity prices and solar panel adoption across Swiss cantons from 2021 to 2024, testing hypotheses about price impacts on renewable energy adoption.

## Data Integration
Combined dataset created from:

```15:23:docs/phase_1.md
The processed dataset (`canton_energy_prices_2021_2024.csv`) contains:
- Canton: Swiss canton name
- Year: Year of observation (2021-2024)
- price_before_surcharge: Combined price (CHF/kWh) of:
  - Grid usage
  - Energy supply costs
  - Community fees
- renewable_surcharge: Feed-in remuneration (KEV) cost
- total_price: Total electricity price
```


## Analysis Methodology

### 1. Correlation Analysis
Examined relationships between:
- Total electricity price vs. solar installation rates
- Price before surcharge vs. adoption rates
- Renewable surcharge impact vs. installation growth

### 2. Multiple Linear Regression Model
Features (X):
- Total electricity price
- Renewable surcharge
- Price change percentage

Target (Y):
- Solar adoption rate (year-over-year installation growth)

## Key Findings

### 1. Model Performance

```263:270:notebooks/canton_energy.ipynb
      "Model Performance:\n",
      "R² Score: 0.183\n",
      "\n",
      "Feature Importance:\n",
      "               Feature  Coefficient\n",
      "0          Total Price     3.584570\n",
      "1  Renewable Surcharge     0.000000\n",
      "2         Price Change    -0.239263\n"
```


### 2. Hypothesis Testing Results

**H1: Higher energy prices correlate with increased solar panel adoption**
- PARTIALLY SUPPORTED
- Evidence:
  - Positive coefficient (3.58) for total price
  - Weak-to-moderate correlation in adoption patterns
  - Limited explanatory power (R² = 0.183)

**H2: Cantons with lower renewable energy tariffs show higher installation rates**
- NOT SUPPORTED
- Evidence:
  - Zero coefficient for renewable surcharge
  - No significant correlation between surcharge levels and adoption rates

### 3. Regional Patterns

```59:62:docs/phase_2.md
### Regional Variations
- Urban cantons show higher absolute numbers
- Rural cantons demonstrate strong per-capita adoption
- Mountain cantons show unique installation patterns due to geographical constraints
```

## Research Questions Answered

1. **How do energy tariffs correlate with renewable energy adoption across Swiss cantons?**
   - Positive but moderate correlation (R² = 0.183)
   - Price increases explain about 18% of adoption variance
   - Other factors likely influence adoption decisions

2. **What impact do canton-specific tariff incentives have on solar panel installations?**
   - Limited direct impact from renewable surcharges
   - Total price more influential than specific incentives
   - Suggests need for revised incentive structures

## Policy Implications

1. **Price Mechanisms**
- Price increases moderately effective for adoption
- Current surcharge structure needs review
- Consider alternative incentive mechanisms

2. **Regional Considerations**
✓
```43:52:docs/phase_2.md
### Regional Leaders
1. **Bern**
   - Consistently highest installation capacity
   - Steady growth throughout the period
   - Strong rural and urban deployment

2. **Zurich**
   - Second-highest adoption rate
   - Accelerated growth post-2022
   - Strong urban infrastructure utilization
```

# Limitations and Future Work

## Current Limitations

### 1. Data Volume Constraints
Our analysis was limited by:
- Only 26 cantons × 4 years (2021-2024) = 104 total observations
- This small sample size significantly impacted our model's reliability (R² = 0.183)
- Annual data points masked monthly variations in both prices and adoption rates
- Limited timeframe may not capture long-term adoption trends or policy effects

### 2. Model Limitations
The linear regression approach showed several weaknesses:
- Assumed linear relationship between price and adoption, missing potential threshold effects
- R² score of 0.183 indicates our model explains only 18.3% of adoption variance
- Annual aggregation lost granular patterns like:
  - Seasonal installation trends
  - Response lag between price changes and adoption decisions
  - Short-term market reactions

### 3. Missing Variables
Critical factors not captured in our analysis:
- Household income levels affect ability to invest
- Property ownership rates influence installation decisions
- Installation costs vary by region and provider
- Local building regulations impact feasibility
- Geographic factors (sun exposure, roof space) affect potential

## Future Work

### 1. Enhanced Data Collection
To address current limitations, future analysis should:
- Expand to monthly granularity for more detailed trends
- Include socioeconomic indicators by canton
- Collect installation cost data
- Track policy changes and incentive programs
- Gather climate and geographic data

### 2. Advanced Modeling
Better capture complex relationships through:
- Time series analysis to model adoption dynamics
- Mixed-effects models to account for canton-specific factors
- Non-linear regression to identify adoption thresholds
- Bayesian methods to handle limited data better

### 3. Additional Analysis
Deepen understanding through:
- Policy effectiveness studies
- Regional clustering analysis
- Installation cost-benefit analysis
- Adoption pattern forecasting
- Canton-specific case studies

This expanded approach would help:
- Improve model accuracy (target R² > 0.5)
- Better explain adoption variations
- Provide more actionable policy insights
- Enable more accurate forecasting

The goal is to move beyond simple price-adoption correlations to a comprehensive understanding of solar adoption drivers in Switzerland.
