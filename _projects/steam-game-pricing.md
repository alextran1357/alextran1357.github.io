---
layout: page
title: Steam Game Pricing Intelligence
description: An API-driven pipeline and Streamlit dashboard for analyzing first-sale timing and discount depth across 8,500+ games.
img: assets/img/projects/steam-pricing.png
github: https://github.com/alextran1357/game-data-tracker
importance: 2
---

## The problem

Game developers and publishers need practical benchmarks for when to run a title's first sale and how deep that discount should be. Public pricing data is incomplete, rate-limited, and recorded as price-change events rather than continuous snapshots.

## My contribution

I built an end-to-end analytical product:

- Combined a curated Steam title set with IsThereAnyDeal metadata and historical pricing APIs.
- Implemented batching, retry logic, response caching, and incremental processing for reliable collection.
- Modeled game metadata, tags, and price history as analysis-ready fact and dimension tables.
- Engineered first-sale timing, sale count, maximum discount, average discount, and lifecycle features.
- Used statistical tests and regression analysis to evaluate pricing and engagement relationships.
- Published an interactive Streamlit dashboard with comparable-game filters and proposed discount benchmarks.

## Decisions and tradeoffs

Because the source API records events rather than daily prices, I modeled the data as an event log and derived lifecycle summaries per game. I documented sampling imbalance and missing metadata rather than overstating how well the dataset represents the entire Steam catalog.

## Results

- Built a dataset covering more than 8,500 games and 460,000 historical price events.
- Created a repeatable pipeline with rate-limit handling and cached recovery.
- Produced a lightweight dashboard dataset suitable for public deployment.
- Translated statistical findings into an interactive decision-support tool.

## Tools

Python, Pandas, REST APIs, Parquet, statistical testing, Streamlit, Altair

[Open the live dashboard](https://alextran1357-game-data-tracker-srcdashboard-u70h5x.streamlit.app/) · [View source](https://github.com/alextran1357/game-data-tracker)
