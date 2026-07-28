---
layout: page
title: California Real Estate Data Pipeline
description: A repeatable cleaning and feature-engineering workflow for monthly residential MLS listing and sales data.
img: assets/img/projects/mls-pipeline.png
github: https://github.com/alextran1357/idx-intern
importance: 3
category: featured
---

## The problem

Monthly MLS exports arrive as separate listing and sales files with inconsistent types, missing values, duplicate information, invalid geography and dates, and extreme property values. Analysts need a trustworthy, reproducible dataset before they can study pricing or market behavior.

## My contribution

As part of the MLS Analytics Program at IDX Exchange, I developed a notebook-based workflow that:

- Aggregates monthly listing and sold exports and retains residential properties.
- Profiles missingness, distributions, invalid values, and duplicate information.
- Joins monthly 30-year fixed mortgage rates from FRED.
- Standardizes types and removes invalid non-California and numeric records.
- Engineers price ratios, price per square foot, calendar fields, listing-to-contract days, and contract-to-close days.
- Applies documented percentile and business-rule thresholds to extreme values.
- Supports Tableau analysis of pricing, sales, days on market, offices, agents, geography, and property types.

## Decisions and tradeoffs

The raw MLS files cannot be published, so the repository documents the complete workflow and preserves representative notebook outputs without exposing source records. Quality flags are created before filtering so questionable records remain explainable rather than disappearing silently.

## Results

- Aggregated 566,673 residential listing records and 414,184 residential sold records in the recorded run.
- Produced final outlier-filtered outputs containing 443,959 listings and 322,807 sales.
- Completed the recorded mortgage-rate join without missing monthly matches.
- Created an analysis-ready foundation for two Tableau dashboards.

## Tools

Python, Pandas, NumPy, Jupyter, Parquet, FRED data, Tableau, Git

[View the documented pipeline](https://github.com/alextran1357/idx-intern)
