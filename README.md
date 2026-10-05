# OpenMeteoWeather
# 🌤️ Open-Meteo Weather Data Pipeline &amp; Analytics 

## Project Summary  
A Databricks data engineering project implementing a Medallion Architecture (Bronze, Silver, Gold) to analyze global weather patterns, seasonal temperature trends, human comfort metrics, and heat anomalies across 20 global locations.

## Overview

This project transforms raw, unstructured REST API responses into business-ready analytical Delta tables. Using multi-layered PySpark and Databricks SQL transformations, the pipeline standardizes daily forecast records, enforces strict schema structures, and aggregates core atmospheric metrics into analytical Gold layer views. Key analytical capabilities include:

* **Heat Anomaly & Window Tracking:** Quantifying daily temperature spikes using 3-day rolling window functions (`OVER PARTITION BY ... ORDER BY`) to detect extreme weather events (>5°C above the moving average).
* **Atmospheric & Solar Analysis:** Evaluating thermal comfort spreads (`temp_max` vs. `sensation_max_temp`), wind intensity, daylight availability, and solar radiation efficiency ratios.
* **City-Level Performance Summaries:** Aggregating historical weather metrics across global climate regions to report temperature extremes, total precipitation, and average daily sunshine hours.

