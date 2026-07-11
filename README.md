# Pollution and Human Development: A 40 Country Analysis


## Overview
This project tests whether national development level and tourism levels are associated with environmental impacts across 40 countries, measured through CO2 emissions, PM2.5 air pollution, and plastic/municipal waste.

## Methodology
Data was manually compiled from 40 countries across six continents from public datasets. Pollution metrics were standardized using z-scores to allow comparison across variables with different units and scales. A composite environmental z-score was created by combining CO2, PM2.5, and waste z-scores.

A linear regression was used between HDI, tourism, and each pollution metric. To test the robustness of these relationships, some regressions were also run with notable outlier countries excluded (countries such as Qatar with skewed CO2 emissions due to oil economy) to see how much they were driving the results.

## Key Findings
 
**Development level is a strong predictor of waste output.**
| Relationship | R² |
|---|---|
| HDI vs. Waste per capita | **0.682** |
| HDI vs. Plastic Waste per capita | **0.338** |
| HDI vs. PM2.5 concentration | **0.270** |
| HDI vs. Composite Pollution Score | 0.174 |
| HDI vs. CO2 per capita | 0.166 |

The strongest relationship found in the dataset was between HDI and waste per capita, there was a positive moderately strong relationship, showing that more developed countries generate more waste per person.
Moreover, the HDI-PM2.5 relationship is negative meaning that more developed countries tend to have measurably cleaner air, even as they produce more waste and CO2. This is notable because it shows that development doesn't affect all forms of pollution the same way.

**While development is a strong predictor of waste output, Tourism volume is a weak predictor of pollution or development.**
| Relationship | R² |
|---|---|
| Tourism vs. HDI | 0.187 |
| Waste vs. Tourism per capita | 0.122 |
| Composite Pollution vs. Tourism | 0.084 |
| CO2 vs. Tourism | 0.089 |
| PM2.5 vs. Tourism | 0.023 |

Across every measure tested in this dataset, tourism showed little power in explaining pollution levels. 
A country's tourism industry size doesn't predict its pollution profile or development level in this dataset to any meaningful amount.

**Outlier sensitivity varies by relationship, not uniformly.**
| Relationship | R² (all) | R² (outliers excluded) |
|---|---|---|
| CO2 vs. Tourism | 0.089 | 0.187 |
| HDI vs. CO2 | 0.166 | 0.022 |
| Waste vs. Tourism | 0.122 | 0.074 |
| Composite Pollution vs. Tourism | 0.084 | 0.165 |
| PM2.5 vs. Tourism | 0.023 | 0.002 |

Furthermore, removing outlier countries affected relationships incosistently. 
Some relationships grew stronger such as CO2 vs Tourism while others such as HDI vs CO2 became weaker.
This suggests that some pollution indicators are largely skewed by a handful of countries. 

## Limitations
This is a correlational analysis of 40 countries, not a controlled study. Relationships shown don't establish causation, and other factors (geography, industry composition, national policy) likely influence these outcomes alongside development level.
A sample of 40 limits how confidently these patterns can be generalized to a larger scale.

## Data Sources
- **HDI**: UNDP Human Development Reports ([hdr.undp.org](https://hdr.undp.org))
- **Population**: World Bank ([data.worldbank.org](https://data.worldbank.org))
- **CO2 emissions per capita**: Our World in Data ([ourworldindata.org](https://ourworldindata.org))
- **PM2.5 concentration**: IQAir World Air Quality Report ([iqair.com](https://iqair.com))
- **Waste per capita**: World Bank "What a Waste" Global Database ([datacatalog.worldbank.org](https://datacatalog.worldbank.org))
- **Tourism data**: UN Tourism Data Dashboard ([untourism.int](https://untourism.int))

## Background
This project began as entry into a data science competition for my highschool as I wanted to try something new. Due to personal circumstrances I stepped away from competing, but I sitll finished the project independently afterwards.
