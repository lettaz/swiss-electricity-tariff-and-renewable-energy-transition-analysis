# Swiss Energy Transition Analysis (2021-2024)

## Project Overview
A comprehensive analysis of Switzerland's energy transition, examining the relationship between electricity tariffs and renewable energy adoption across cantons from 2021 to 2024. The project spans three phases, each building upon previous findings to create a complete understanding of price-driven solar adoption patterns.

## Research Questions & Hypotheses

### Core Questions
1. How do energy tariffs correlate with renewable energy adoption across Swiss cantons?
2. What impact do canton-specific tariff incentives have on solar panel installations?

### Hypotheses
- H1: Higher energy prices correlate with increased solar panel adoption
- H2: Cantons with lower renewable energy tariffs show higher installation rates

## Key Findings

### Phase 1: Electricity Tariff Analysis
[Detailed documentation in docs/phase_1.md]
- Base price average: 0.2060 CHF/kWh
- Renewable surcharge: 0.0230 CHF/kWh (consistent)
- Total price average: 0.2290 CHF/kWh
- Significant price increases between 2022-2023
- Regional variations in grid usage costs

### Phase 2: Solar Adoption Patterns
[Detailed documentation in docs/phase_2.md]
- Total installed capacity: 15,115,209.50 kWp
- Mean yearly installation: 145,338.55 kWp
- Regional leaders: Bern and Zurich
- Significant acceleration in 2023-2024

### Phase 3: Correlation Analysis
[Detailed documentation in docs/phase_3.md]
- Model Performance: R² = 0.183
- Total Price Impact: Positive coefficient (3.584570)
- Renewable Surcharge: No significant impact (0.000000)
- Price Change Effect: Slight negative (-0.239263)

## Methodology

### Data Integration
Combined analysis of:
- ElCom Electricity Tariff Dataset
- Canton Solar Installation Records
- Renewable Surcharge Implementation Data

## Results Summary

### Hypothesis Testing Results
1. H1 (Price Impact): PARTIALLY SUPPORTED
   - Positive correlation with total price
   - Limited explanatory power (18.3%)

2. H2 (Tariff Effect): NOT SUPPORTED
   - No significant correlation
   - Suggests need for alternative incentives

## Limitations & Future Work

### Current Constraints
1. Data Volume:
   - 26 cantons × 4 years
   - Annual granularity masks patterns
   - Limited timeframe

2. Model Performance:
   - R² = 0.183 indicates additional factors
   - Linear assumptions may not capture complexity
   - Missing socioeconomic variables

### Future Directions
[Detailed in docs/phase_3.md]
1. Enhanced Data Collection
2. Advanced Modeling Approaches
3. Additional Analysis Methods

## Data Sources
- Median Electricity Tariff Dataset (ElCom)
- Energy Reporter Dataset

## Contributing
Contributions welcome! Please review our contributing guidelines.

## License
MIT License

## Documentation References
- Phase 1: `/docs/phase_1.md` - Electricity Tariff Analysis
- Phase 2: `/docs/phase_2.md` - Solar Adoption Analysis
- Phase 3: `/docs/phase_3.md` - Correlation Analysis