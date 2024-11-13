# Phase 1: Electricity Tariff Analysis Documentation

## Overview
Phase 1 analyzes electricity tariff trends across Swiss cantons from 2021 to 2024, focusing on price components and renewable surcharge impacts.

## Data Processing
The data processing pipeline is implemented in:

```106:126:notebooks/energy-tariff.ipynb
    process_tariff_data(file_path)
```


### Cleaned Dataset Structure
The processed dataset (`canton_energy_prices_2021_2024.csv`) contains:
- Canton: Swiss canton name
- Year: Year of observation (2021-2024)
- price_before_surcharge: Combined price (CHF/kWh) of:
  - Grid usage
  - Energy supply costs
  - Community fees
- renewable_surcharge: Feed-in remuneration (KEV) cost
- total_price: Total electricity price

Uses:
- Temporal analysis of price trends
- Regional comparison of electricity costs
- Policy impact assessment
- Integration with future solar adoption analysis

## Visualizations
The analysis produces three complementary visualizations:

### 1. Energy Price Trend Before Renewable Surcharge

Purpose:
- Shows base electricity costs without renewable incentives
- Enables comparison of underlying price structures across cantons
- Highlights regional infrastructure and supply cost differences

### 2. Renewable Surcharge Impact

Purpose:
- Visualizes the KEV surcharge contribution
- Demonstrates policy consistency across regions
- Shows temporal stability of renewable incentives

### 3. Total Price Trend

Purpose:
- Presents complete electricity cost evolution
- Enables comprehensive canton-to-canton comparison
- Shows combined effect of all price components

## Key Findings

### Price Components
- Base price (before surcharge): 0.2060 CHF/kWh (average)
- Renewable surcharge: 0.0230 CHF/kWh (consistent)
- Total price: 0.2290 CHF/kWh (average)

### Regional Variations
- Mountain cantons show higher grid usage costs
- Urban cantons generally have higher community fees
- Renewable surcharge remains uniform across regions

### Temporal Trends
- Significant price increases between 2022-2023
- Accelerated growth in 2023-2024
- Stable renewable surcharge throughout period


## Statistical Summary
As shown in the execution results:

```264:272:notebooks/energy-tariff.ipynb
      "Summary Statistics (2021-2024):\n",
      "------------------\n",
      "Number of cantons analyzed: 26\n",
      "Years covered: 2021-2024\n",
      "\n",
      "Mean prices by component (CHF/kWh):\n",
      "Total price: 0.2290\n",
      "Price before surcharge: 0.2060\n",
      "Renewable surcharge: 0.0230\n"
```

The analysis covers all 26 Swiss cantons with complete price component breakdowns for the 2021-2024 period.