---
layout: page
title: Website Performance Benchmarking
description: A PageSpeed pipeline and decision-support tool that evolved from XGBoost scenario modeling into peer benchmarking and performance prioritization.
img: assets/img/projects/site-speed.png
github: https://github.com/alextran1357/site_speed_recommendation
importance: 4
---

## The problem

Lighthouse and PageSpeed Insights provide detailed audits, but non-technical users still struggle to determine whether a result is unusually poor and which area deserves attention first. I initially approached the problem by predicting how resource changes could affect Largest Contentful Paint (LCP), then reframed it after recognizing that a model estimate does not prove what a real optimization will cause.

## My contribution

I developed the project through two connected iterations:

- Collected and prepared approximately 16,000 usable PageSpeed lab-data rows.
- Trained and evaluated regression and boosting models, including separate mobile and desktop experiments.
- Built a Streamlit scenario planner that estimates how LCP could change as selected resource metrics improve.
- Added category-based peer benchmarking and percentile comparisons instead of relying on one universal threshold.
- Ranked likely investigation areas across JavaScript, images, third-party code, layout, and resource delivery.

## Decisions and tradeoffs

An earlier XGBoost iteration reached approximately 1.35 seconds MAE and an R² of 0.86 on the recorded test split. I also found and removed a leakage-prone feature, tested target transformations, and separated mobile from desktop because their error patterns differed. Those results were useful for scenario exploration, but they could not guarantee the effect of a real optimization. I therefore positioned the final product as benchmarking and decision support, with every recommendation requiring validation through a fresh audit after changes are deployed.

## Outcome

The project now tells one coherent story from modeling to product judgment: use the model to explore plausible scenarios, use peer benchmarks to prioritize unusually weak areas, and use a new PageSpeed audit to measure the outcome of real changes.

## Tools

Python, Pandas, XGBoost, scikit-learn, Databricks, Streamlit, Google PageSpeed Insights API, Lighthouse metrics

[View source](https://github.com/alextran1357/site_speed_recommendation)
