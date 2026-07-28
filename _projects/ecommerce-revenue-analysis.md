---
layout: page
title: E-commerce Revenue Analytics
description: Revenue modeling, product-mix analysis, Power BI reporting, and Prophet forecasting across 1.9 million order items.
img: assets/img/projects/ecommerce-analytics.png
github: https://github.com/alextran1357/ecommerce-revenue-analysis
importance: 1
category: featured
---

## The problem

A multi-year e-commerce dataset contained more than one million orders and 1.9 million item-level records, but its nested fields, inconsistent product labels, promotional items, and duplicated time columns made direct business analysis unreliable.

## My contribution

I owned the workflow from raw export to decision-ready analysis:

- Parsed nested JSONL fields with Python and separated the data into customer, order, and order-item tables.
- Built a calendar model and reusable measures with Power Query, Power Pivot, and DAX.
- Investigated missing timestamps, inconsistent product categories, and approximately 500,000 zero-price promotional records.
- Created Excel and Power BI reporting for revenue growth, product contribution, pricing, and order volume.
- Built and cross-validated a Prophet time-series forecast.

## Decisions and tradeoffs

I kept verified promotional products rather than treating every zero-price record as an error. I also evaluated forecasting failures around short promotional spikes separately from normal seasonal demand, because those events were not explained well by trend and seasonality alone.

## Results

- Analyzed 326,673 customers, 1,018,641 orders, and 1,901,304 order items.
- Identified approximately $78.7 million in total revenue across the analysis period.
- Found that gummies generated approximately 76% of revenue, creating product concentration risk.
- Found that Q4 generated roughly 35% of annual revenue.
- Achieved approximately 15–18% MAPE in time-series cross-validation.

## Selected outputs

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/projects/ecommerce-dashboard.png" title="Power BI year-over-year revenue dashboard" alt="Power BI dashboard showing year-over-year e-commerce revenue performance" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/projects/ecommerce-revenue-trend.png" title="Monthly revenue trend" alt="Monthly e-commerce revenue trend chart" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Power BI reporting and the monthly revenue trend used to communicate growth, product mix, and seasonality.
</div>

## Tools

Python, Excel, Power Query, Power Pivot, DAX, Power BI, Prophet

[View source and full analysis](https://github.com/alextran1357/ecommerce-revenue-analysis)
