# startup-market-analysis
Analysis of dataset as part of a capstone project for a Python Data Analyst program by Excelerate Malaysia.

# Venture Analytics: Global Startup Landscape
## Project Overview
This project performs an exploratory data analysis (EDA) of the global startup ecosystem, integrating firm-level valuation data with country-level macroeconomic indicators. The goal is to identify investment hotspots, assess industry trends, and determine how macroeconomic factors (like GDP and inflation) correlate with startup success.

## Target Audience
Venture capital investors, policymakers, and economic researchers.

## Business Problem
Investors and policymakers often look at startups in isolation. This project seeks to contextualize startup performance within the broader economic environment. Key questions addressed include:
- Do developed or emerging markets offer the highest capital efficiency for startups?
- How do valuation multiples (e.g., Revenue Multiples) vary across industries like AI/ML vs. Logistics?

# Data Pipeline
The analysis merges two distinct datasets to create a unified view of the ecosystem:

## Dataset of startups, sourced from Kaggle.
* Key Metrics: `funding_amount_usd`, `estimated_valuation_usd`, `estimated_revenue_usd`, `industry`.
* Preprocessing: Removed unneccesary columns and engineered a Revenue Multiple metric (Valuation / Revenue) to gauge market sentiment.

## Macroeconomic Indicators, sourced from World Bank website
- Key Metrics: GDP_per_capita, Inflation_CPI, R&D_Expenditure, Unemployment_Rate.
- Preprocessing: Imputed missing R&D values using external data (Visual Capitalist) and filtered for Top 10 startup hubs (USA, UK, Singapore, etc.) for comparative analysis.

# Tech Stack
- Language: Python
- Data Manipulation: Pandas, NumPy
- Visualization: Seaborn, Matplotlib

Analysis: Correlation heatmap, scatter plots, bar charts

Key Insights & Methodology
* Valuation Analysis: Calculated "Revenue Multiples" to compare hype vs. reality across sectors. (e.g., AI/ML startups showed higher mean multiples than the other industries, indicating high future growth expectations).
* Macro-Correlation: Merged datasets to test the hypothesis that higher national R&D expenditure leads to higher average startup revenues.
* Sector Dominance: Analyzed funding distribution to find that countries like Singapore show high efficiency in Fintech and AI capital deployment.
