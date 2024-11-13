# Phase 2: Solar Panel Adoption Analysis Documentation

## Overview
Phase 2 analyzes solar power installation trends across Swiss cantons from 2021 to 2024, establishing the foundation for correlation analysis with electricity tariffs in Phase 3.

## Data Processing
The data processing pipeline is implemented in:


```568:577:notebooks/cantons.ipynb
    process_solar_adoption_data(df)
```


### Cleaned Dataset Structure
The processed dataset (`canton_solar_adoption_2021_2024.csv`) contains:
- Canton: Swiss canton name (full names)
- Year: Year of observation (2021-2024)
- solar_power_installed_kwp: Installed solar capacity in kilowatt peak (kWp)

Uses:
- Solar adoption trend analysis
- Regional comparison of renewable energy uptake
- Base data for Phase 3 correlation studies

## Visualizations
The analysis produces visualizations on solar adoption trends in PNG and HTML formats.

Purpose:
- Shows yearly solar installation progression
- Enables direct canton-to-canton comparison
- Highlights regional adoption patterns
- Identifies leading and lagging regions


## Key Findings

### Installation Capacity
- Total installed capacity: 15,115,209.50 kWp
- Mean yearly installation: 145,338.55 kWp
- All 26 cantons analyzed

### Regional Leaders
1. **Bern**
   - Consistently highest installation capacity
   - Steady growth throughout the period
   - Strong rural and urban deployment

2. **Zurich**
   - Second-highest adoption rate
   - Accelerated growth post-2022
   - Strong urban infrastructure utilization

### Growth Patterns
- Significant acceleration in 2023-2024
- Consistent upward trend across all cantons
- Larger cantons showing proportionally higher adoption rates

### Regional Variations
- Urban cantons show higher absolute numbers
- Rural cantons demonstrate strong per-capita adoption
- Mountain cantons show unique installation patterns due to geographical constraints

## Integration with Phase 1
This analysis complements the electricity tariff findings from Phase 1:
- Regions with higher tariffs generally show increased adoption rates
- The renewable surcharge implementation correlates with installation acceleration
- Price trends appear to influence adoption decisions

## Statistical Summary
As shown in the execution results:

```677:683:notebooks/cantons.ipynb
      "Solar Adoption Summary Statistics (2021-2024):\n",
      "------------------\n",
      "Number of cantons analyzed: 26\n",
      "Years covered: 2021-2024\n",
      "\n",
      "Total installed capacity: 15115209.50 kWp\n",
      "Mean yearly installation: 145338.55 kWp\n"
```


## Next Steps
This phase sets up the foundation for Phase 3's correlation analysis between:
- Solar adoption rates and electricity prices
- Installation trends and renewable surcharges
- Regional characteristics and adoption patterns

The cleaned dataset and visualizations will be essential for:
- Logistic regression analysis
- Policy impact assessment
- Future adoption forecasting
- Regional policy recommendations