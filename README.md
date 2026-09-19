# Employment and Mobility Patterns in Counties of England & Wales (2011) with Age Comparison to 2021

![Dashboard](Interactive%20Tableau%20workbook/dashboard.png)

## Overview

This project investigates socio-economic and mobility patterns across county-level local authorities in England and Wales using UK Census data. The analysis combines demographic, economic, transportation, and vehicle ownership indicators from the 2011 Census with age structure data from the 2021 Census to explore regional disparities and demographic changes over a decade.

The project applies dimensionality reduction, K-Means clustering, Bayesian analysis, and interactive visual analytics to identify distinct socio-economic profiles across 174 county-level local authorities.

## Objectives

- Examine regional differences in employment, mobility, car ownership, and age structure.
- Compare age demographics between 2011 and 2021.
- Identify underlying socio-economic patterns using dimensionality reduction techniques.
- Group county-level local authorities into meaningful socio-economic clusters.
- Explore probabilistic relationships between socio-economic variables using Bayesian methods.
- Present findings through an interactive Tableau dashboard.

## Dataset

The analysis uses UK Census data for England and Wales at the county-level local authority scale.

### 2011 Census

- Age Structure
- Economic Activity
- Distance Travelled to Work
- Car Ownership

### 2021 Census

- Age Structure (used for decade-long demographic comparison)

### Coverage

- 174 County-Level Local Authorities
- England and Wales

## Data Preparation

The original census datasets contained detailed variables that were aggregated into broader socio-economic indicators:

- Individual age bands → Youth, Working-Age, and Retired Population
- Detailed commute distances → Short, Medium, and Long Commutes
- Vehicle ownership categories → Car Ownership Indicators
- Economic activity classes → Employment Activity Indicators

Both absolute counts and proportional measures were analysed to account for differences in population size across local authorities.

## Methodology

### 1. Data Transformation

- Data cleaning and preprocessing
- Feature aggregation
- Standardisation and normalization

### 2. Dimensionality Reduction

Three dimensionality reduction techniques were explored:

- Principal Component Analysis (PCA)
- t-Distributed Stochastic Neighbor Embedding (t-SNE)
- Uniform Manifold Approximation and Projection (UMAP)

UMAP was selected as the primary dimensionality reduction technique because it provided a useful low-dimensional representation of the high-dimensional feature space for subsequent clustering and visualisation.

### 3. Clustering Analysis

The UMAP representation was used as the input for **K-Means clustering** to identify socio-economic groupings across county-level local authorities.

Four clusters were identified in the final clustering solution.

### 4. Bayesian Analysis

Bayesian analysis was used to examine probabilistic relationships between demographic, economic, commuting, and vehicle ownership variables.

The posterior distributions indicated:

- A positive relationship between economic participation and shorter commuting distances, particularly for residents living within 30 km of their workplace.
- A negative relationship between the proportion of retired-age residents and overall economic activity.
- A negative relationship between unemployment rates and economic activity.
- Car ownership was an important component of the socio-economic profile, while proximity to employment showed a stronger predictive relationship with the working population than vehicle ownership alone.

The Bayesian analysis also provided estimates of uncertainty around these relationships, allowing the strength and direction of the observed associations to be assessed.

### 5. Visual Analytics

An interactive Tableau dashboard was developed to enable:

- Regional comparisons
- Cluster exploration
- Geographic analysis
- Temporal age comparisons
- Interactive filtering and drill-down

## Identified Clusters

### Cluster 1: Ageing, Long Commute Workforce

- Older population structure
- Longer commuting distances
- Lower local employment accessibility

### Cluster 2: Locally Employed, Mixed Mobility Communities

- Strong local employment patterns
- Diverse mobility behaviour
- Balanced socio-economic indicators

### Cluster 3: High Employment, High Mobility, Multi-Car Areas

- High economic activity
- Greater mobility
- Higher rates of multi-car ownership

### Cluster 4: Low Mobility, Car-Limited Areas

- Lower vehicle ownership
- Reduced mobility
- Potentially constrained access to employment opportunities

## Key Findings

### Employment and Mobility

- Regions with higher economic activity generally exhibited greater mobility.
- Shorter commuting distances showed a positive relationship with economic participation, particularly within the 30 km range examined in the Bayesian analysis.
- Car ownership formed an important part of the socio-economic profiles identified through the analysis.
- The Bayesian analysis indicated a stronger predictive relationship between proximity to employment and the working population than vehicle ownership alone.

### Demographic Change

- Comparison of 2011 and 2021 age structures indicates a general shift towards older population structures across several local authorities.
- Several regions experienced noticeable changes in their age composition over the decade.

### Spatial Patterns

- The mapped cluster assignments show geographic concentration across parts of England and Wales.
- Central England contains many high-employment, high-mobility areas.
- Parts of Wales, Northern England, and South-West England display ageing populations and longer commuting patterns.

## Technologies and Methods

### Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- UMAP
- Tableau

### Methods

- Principal Component Analysis (PCA)
- t-SNE
- UMAP
- K-Means Clustering
- Bayesian Analysis
- Interactive Data Visualisation

## Learning Outcomes

- Census data integration and transformation
- High-dimensional data analysis
- Dimensionality reduction
- Unsupervised clustering
- Bayesian statistical reasoning
- Interactive visual analytics
- Information visualisation design principles
- Tableau dashboard development

## Repository Structure

### Cleaned / Transformed Data

- `Data21-11.csv` — Combined dataset used for longitudinal analysis (2011–2021)
- `Preprocessed Data.csv` — Final cleaned dataset used for modelling and clustering

### Raw Census Data

- `Aggregate_Data.csv` — Aggregated socio-economic indicators
- `Car_or_van.csv` — Car/van ownership
- `Distance_travelled_to_work.csv` — Distance travelled to work
- `Population_Age.csv` — 2011 age structure
- `census2021-ts007-utla (Age).csv` — 2021 age structure
- `economic_activity.csv` — Economic activity

### Final Report

- `fp25098_Report.pdf`

### Tableau

- `fp25098_Tableau.twbx`

### Notebooks

- `Baysian_Posterior_Distribution.ipynb`
- `Dimensionality_Reduction.ipynb`

### Other

- `README.md`

## Author

**Aman Singh**  
MSc Data Science Student  
University of Bristol
