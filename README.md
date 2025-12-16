# Demand Forecasting and Scenario Planning

## Purpose
This project demonstrates end-to-end demand forecasting with uncertainty quantification and scenario analysis, translating statistical outputs into clear operational planning guidance. It is designed to reflect how economists support planning, capacity, and inventory decisions in data-driven organizations.

## Business Context
Accurate demand forecasts are necessary but insufficient for decision-making under uncertainty. This project focuses on producing reliable short-horizon forecasts, quantifying forecast uncertainty using prediction intervals, stress-testing outcomes under alternative demand scenarios, and converting results into actionable planning insights. The workflow mirrors real-world economist contributions in operations, supply chain, and planning teams.

## Data
The analysis uses a synthetic univariate demand time series at a monthly frequency representing aggregate demand. Preprocessing includes missing-value checks, a train–validation split, and basic stationarity diagnostics. The dataset is stored at data/demand_series.csv.

## Methodology
Exploratory time series analysis examines trend, seasonality, autocorrelation (ACF), and partial autocorrelation (PACF). Forecasting is performed using a Seasonal ARIMA (SARIMA) model, with model selection informed by diagnostics and validation performance. Forecast accuracy is evaluated using Root Mean Squared Error (RMSE), Mean Absolute Percentage Error (MAPE), and Symmetric Mean Absolute Percentage Error (sMAPE). Uncertainty is explicitly quantified through prediction intervals. Scenario planning compares baseline, high-demand, and low-demand trajectories to support operational decision-making.

## Outputs
The project produces a forecast plot with prediction intervals, a table of error metrics, and a scenario comparison plot. All outputs are saved in the outputs/ directory as forecast_plot.png, metrics.csv, and scenarios.png.

## Key Insights
Prediction intervals widen as the forecast horizon increases, highlighting planning risk. Scenario overlays show that even modest demand shifts can materially affect capacity and inventory requirements. Point forecasts alone understate operational uncertainty and can lead to under- or over-allocation of resources.

## Implications for Planning
Planning decisions should rely on prediction intervals rather than point estimates when setting capacity buffers. Scenario analysis enables stress-testing of inventory and staffing plans under demand volatility. Short-horizon forecasts should be updated frequently as new information becomes available. These principles generalize across retail, logistics, and platform-based demand environments.

## Tech Stack
The analysis is implemented in Python using pandas, numpy, statsmodels, scikit-learn, and matplotlib, and executed in a Jupyter Notebook environment.

## Repository Structure
The repository includes a data folder containing the demand time series, a notebooks folder containing the SARIMA forecasting notebook, an outputs folder containing generated plots and metrics, and this README file documenting the project.

## Notes
This project emphasizes interpretability, validation discipline, and decision relevance over model complexity. The approach is intentionally transparent and reproducible to support economist-style communication and review.

## Author
Vamakshi Chaturvedi | Economics | Forecasting | Decision Support
