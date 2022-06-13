---
tags: [project]
---

[GitHub repository](https://github.com/pawaclawczyk/prototypes/tree/main/budget_pacing)

The project provides budget spending simulation framework to compare different budgeting algorithms.

There are two algorithms implemented:
- ASAP - spending budget as fast as possible.
- Throttled algorithm based on the LinkedIn paper, which tries to follow the forecast and actual impressions delivery.

Further algorithms that could be implemented are:
- Even budget split over N period during a day - it assumes dividing daily budget into N equal chunks, e.g. 28 budget chunks representing 5 minut periods, and then spending is chunk in ASAP-style.

The ASAP and even budget split are commonly used, and they do not take any forecasted, nor actual, traffic into account.

### Hypothesis

- In the throttled case the campaign should be exposed during a longer period of time.

- If the traffic volume is significantly larger than forecast, then the revenue in the throttled case should be bigger than in the ASAP case.
	- In other cases, ASAP should produce highest revenue value.

### Technology

The simulation and analysis tasks will be executed using [Dagster](../pages/Dagster.md).
