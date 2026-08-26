# Tech Layoffs Analyst | Data Analyst Self Learning Project

# Tech Layoffs Analysis (2020–2025)

A data analyst portfolio project analyzing global tech industry layoffs from 2020 to 2025, exploring trends over time, geographic and industry impact, and the relationship between company funding stage / capital raised and layoff severity.

## 📊 Project Overview

| | |
|---|---|
| **Type** | Exploratory Data Analysis (EDA) & Data Visualization |
| **Tools** | Python, pandas, matplotlib, seaborn |
| **Dataset** | [Tech Layoffs Dataset (Kaggle)](https://www.kaggle.com/datasets/ulrikeherold/tech-layoffs-2020-2024), 1,745 layoff events, 2020–2025 |
| **Notebook** | [`notebooks/tech_layoffs_analysis.ipynb`](notebooks/tech_layoffs_analysis.ipynb) |

## 🎯 Objectives

1. How have layoffs trended year over year since 2020?
2. Which countries and regions have been hit hardest?
3. Which industries have the largest layoffs?
4. Is there a relationship between funding stage and layoff severity?
5. Does capital raised predict how deeply a company cuts its workforce?
6. Which companies had the largest single layoff events?

## 🔑 Key Insights

- **Layoffs move in waves, not a steady climb.** Two clear peaks stand out: 2020 (COVID-19 shock) and 2023 (post-pandemic hiring correction). 2021 was the calm before the storm; 2024–2025 remain above pre-2022 levels.
- **The US and India account for the largest share of layoffs**, reflecting where major tech employers concentrate headcount, both at HQ and in offshore hubs.
- **"Tech layoffs" span far more than software companies**, fintech (labeled "Finance"), retail-tech, and healthcare-adjacent firms rank among the hardest-hit sectors.
- **Post-IPO companies drive the largest absolute numbers**, but early-stage startups tend to cut a larger *percentage* of their (smaller) workforce per event.
- **Capital raised is a weak predictor of layoff severity**, being well-funded doesn't protect a company from deep cuts.
- **A handful of mega-cap layoff events skew all headline totals**, the median event is modest (15 employees), but the largest single event cut 22,000.

## 🗂️ Repository Structure

```
tech-layoffs-portfolio/
├── data/
│   ├── Cleaned_tech_layoffs.csv              # Primary dataset used in analysis
│   ├── tech_layoffs_til_2025.csv             # Larger raw file, used for cross-check
│   └── layoffs_location_with_coordinates.csv # Location reference table
├── notebooks/
│   └── tech_layoffs_analysis.ipynb           # Full analysis notebook
└── README.md
```

## 🛠️ How to Run

```bash
pip install pandas matplotlib seaborn jupyter
jupyter notebook notebooks/tech_layoffs_analysis.ipynb
```

## 📌 Limitations

- The dataset tracks *announced* layoff events only, it does not capture quiet attrition, hiring freezes, or unannounced reductions.
- `Stage` and `Money_Raised_in__mil` have some missing values, kept as `Unknown` / excluded rather than dropped to preserve otherwise valid records.

## 🔮 Possible Next Steps

- Build a regression/classification model to predict layoff severity from company attributes.
- Add a geographic map visualization using the provided coordinate file.

---
*This is a personal portfolio project built for practicing data analysis and visualization skills.*
