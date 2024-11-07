# README.md

## Electricity Tariff Analysis Project in Switzerland

### Project Overview
This project analyzes the relationship between electricity tariffs and renewable energy adoption across Swiss cantons, focusing on data from March 2021 to August 2024.

### Data Processing & Analysis Components

#### 1. Data Cleaning and Transformation
```python
startLine: 83
endLine: 136
```
- Standardizes column names for easier analysis
- Converts currency from Rappen to CHF
- Extracts profile codes (H1-H8, C1-C6) from descriptions
- Categorizes consumers into Household/Commercial
- Maps annual consumption volumes to profiles

#### 2. Tariff Component Analysis
```python
startLine: 138
endLine: 153
```
This analysis helps address hypothesis H1 ("The higher the energy price, the more solar panel adoption there is") by:
- Breaking down electricity costs by components (energy, grid, taxes, renewable surcharge)
- Calculating statistical measures (mean, std, min, max) per canton
- Enabling comparison of tariff structures across regions

#### 3. Temporal Analysis
```python
startLine: 157
endLine: 182
```
Supports both hypotheses by:
- Tracking price trends over time
- Identifying seasonal patterns in electricity pricing
- Enabling analysis of how tariff changes affect adoption rates
- Grouping data by months and seasons for pattern recognition

#### 4. Consumption Profile Analysis
```python
startLine: 186
endLine: 198
```
Helps understand:
- How different consumer types are affected by tariffs
- Price variations across consumption profiles
- Impact of consumption patterns on total costs

### Visualizations

The code generates three key visualizations:

1. **Tariff Components Distribution** (`tariff_components_distribution.png`)
   - Four boxplots showing distribution of each price component by canton
   - Helps identify regional pricing variations and outliers
   - Useful for comparing tariff structures across regions

2. **Canton Comparison** (`canton_comparison.html`)
   - Interactive boxplot showing total price distribution
   - Segmented by canton and consumption profile
   - Helps identify regional pricing patterns and consumer impacts

3. **Monthly Price Trends** (`temporal_trends.html`)
   - Interactive line plot showing price evolution over time
   - Color-coded by canton
   - Useful for identifying temporal patterns and regional differences

### Data Export
The cleaned dataset is exported to 'cleaned_electricity_tariffs.csv' for:
- Further analysis in other tools
- Sharing with stakeholders
- Integration with additional datasets (e.g., solar adoption data)

### Key Findings from Initial Analysis

#### 1. Tariff Component Distribution
- **Energy Price Variations**
  - Highest mean energy prices: Fribourg (0.104 CHF/kWh) and Neuchâtel (0.098 CHF/kWh)
  - Lowest mean energy prices: Nidwalden (0.067 CHF/kWh) and Schaffhausen (0.078 CHF/kWh)
  - Most cantons maintain energy prices between 0.085-0.095 CHF/kWh

- **Grid Usage Pricing**
  - Highest grid usage costs: Glarus (0.108 CHF/kWh) and Uri (0.102 CHF/kWh)
  - Lowest grid usage costs: Valais (0.072 CHF/kWh) and Geneva (0.077 CHF/kWh)
  - Significant variation in grid usage prices suggests different infrastructure costs across regions

- **Community Fees (Taxes)**
  - Basel Stadt stands out with significantly higher taxes (0.066 CHF/kWh)
  - Several cantons (Appenzell Innerrhoden, Fribourg, Schaffhausen) have zero or minimal taxes
  - Most cantons maintain taxes below 0.010 CHF/kWh

- **Renewable Surcharge**
  - Remarkably consistent across most cantons (around 0.019 CHF/kWh)
  - Slight variations in Geneva, Basel Stadt, and Nidwalden (0.016-0.017 CHF/kWh)
  - Suggests standardized federal policy for renewable energy support

#### 2. Consumption Profile Analysis
- **Household vs Commercial Patterns**
  - Small households (H1, H2) face highest total prices (0.268 and 0.245 CHF/kWh respectively)
  - Large commercial consumers (C5-C7) benefit from lowest rates (0.154-0.170 CHF/kWh)
  - Clear economy of scale in pricing structure

- **Grid Usage Impact**
  - Grid usage costs show largest variation between consumer types
  - Small households (H1) pay highest grid usage (0.141 CHF/kWh)
  - Large commercial users (C6) pay lowest grid usage (0.053 CHF/kWh)

#### Initial Implications for Renewable Energy Adoption
1. **Price Incentive Structure**
   - Higher residential rates might incentivize household solar adoption
   - Commercial users might need additional incentives due to lower baseline costs

2. **Regional Variations**
   - Cantons with higher energy prices (e.g., Fribourg, Neuchâtel) might see faster solar adoption
   - Low-tax regions might have more disposable income for renewable investments

3. **Policy Consistency**
   - Uniform renewable surcharge suggests coordinated federal approach
   - Might need canton-specific incentives to address local pricing variations

### Next Steps for Project Extension
1. Add solar panel installation data to correlate with tariff data
2. Include canton-specific renewable energy incentives
3. Add geospatial visualizations for regional patterns
4. Create year-over-year comparison of adoption rates
5. Add statistical tests for hypothesis validation

