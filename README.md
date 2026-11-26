# CO₂ Emissions in Nigeria: Time Series Modelling and Forecasting (1980-2024)

Final year project by **Victor Kehinde**, Department of Statistics, University of Ibadan. Supervised by Dr. Otekurin.

## The question

Nigeria emitted about 136 million tonnes of CO₂ in 2024, and the figure keeps rising. This project asks two things: what drives emissions in the long run, and how well can we forecast them to 2030?

## What I did

- Described the emission trend over 45 years of annual data
- Tested for a long-run link between emissions, population, GDP per capita and energy use (ARDL bounds test)
- Measured the long-run effects and how fast emissions correct after a shock
- Compared ARIMA and ARDL forecasts on a hold-out period, 2020 to 2024

## Main findings

| Result | Value |
|---|---|
| Bounds test F-statistic | 5.10 (long-run link confirmed at 1%) |
| Speed of adjustment | -0.47 (about 47% of a gap closes each year) |
| Population elasticity | 2.03 (strongest long-run driver) |
| GDP per capita elasticity | -1.13 |
| Energy per capita elasticity | -0.42 (not significant) |
| Forecast error, ARIMA vs ARDL | 4.86%
