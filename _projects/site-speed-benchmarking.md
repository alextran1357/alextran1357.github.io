---
layout: page
title: Website Performance Benchmarking
description: A business-facing dashboard that compares Lighthouse results with peer sites and prioritizes likely performance bottlenecks.
img: assets/img/projects/site-speed.png
github: https://github.com/alextran1357/site_speed_recommendation
importance: 4
---

## The problem

Lighthouse and PageSpeed Insights provide detailed performance audits, but non-technical users still struggle to determine whether a result is unusually poor and which area deserves attention first.

## My contribution

I reframed an early prediction idea into a more useful benchmarking product:

- Collected Lighthouse and PageSpeed Insights metrics for websites across categories.
- Compared individual sites with relevant peers rather than using one universal threshold.
- Ranked likely investigation areas across JavaScript, images, third-party code, layout, and resource delivery.
- Built a Streamlit interface with plain-language explanations.
- Added a scenario planner that estimates how Largest Contentful Paint could change when resource metrics move toward stronger peer percentiles.

## Decisions and tradeoffs

The scenario planner is presented as a planning estimate, not a guaranteed post-optimization result. Recommendations remain tied to observed peer distributions and should be validated through a fresh audit after real changes are deployed.

## Outcome

The project turns a technical audit into a business-facing benchmark and prioritization workflow, combining performance data, statistical comparison, and actionable communication.

## Tools

Python, Pandas, scikit-learn, Streamlit, Google PageSpeed Insights API, Lighthouse metrics

[View source](https://github.com/alextran1357/site_speed_recommendation)
