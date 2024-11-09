# Flight Delay Prediction Project

This project aims to predict flight delays using historical weather and flight data. By analyzing weather conditions, it provides insights for travelers and airlines on potential delays, utilizing both deterministic and probabilistic models.

## Project Overview

Flight delays are often caused by weather, air traffic, and airport limitations. This project models these delays with a focus on weather conditions, using historical data for flights between:
- **Origin Airport**: Chicago O'Hare International (ORD), Chicago, IL
- **Destination Airport**: Hartsfield-Jackson Atlanta International (ATL), Atlanta, GA
- **Airline**: Delta Airlines Inc. (DL)
- **Weather Data**: Collected from ATL, covering temperature, precipitation, wind speed, and visibility (2017-2024)

## Project Structure

- `data/`: Contains raw and processed flight and weather datasets.
- `project.ipynb`: Jupyter notebooks for data processing, feature engineering, and model building.
- `requirements.txt`: List of required libraries.

## Methodology

1. **Data Processing**: Load, clean, and merge datasets for flight schedules, delays, and weather conditions.
2. **Feature Engineering**: Create delay indicators, weather-related features, and encode categorical variables.
3. **Model Building**:
   - **Deterministic Model**: Uses Logistic Regression as a baseline.
   - **Probabilistic Model (Monte Carlo)**: Introduces random weather variations to account for uncertainty.
4. **Model Evaluation**: Assesses accuracy, precision, recall, and ROC AUC scores.

## Model Performance

| Metric          | Deterministic Model | Probabilistic Model |
|-----------------|---------------------|----------------------|
| **Accuracy**    | 94.56%              | 94.63%              |
| **Precision**   | 96.27%              | 96.28%              |
| **Recall**      | 91.92%              | 92.07%              |
| **ROC AUC**     | 99.03%              | 99.04%              |

The probabilistic model slightly outperforms the deterministic approach, suggesting better handling of delay sensitivity with uncertainty.

## Potential Improvements

1. **Feature Expansion**: Add data on air traffic, airport logistics, and operational schedules.
2. **Enhanced Uncertainty Techniques**: Use Bayesian Neural Networks or Gaussian Processes.
3. **Real-Time Weather Updates**: Integrate dynamic weather data for responsiveness.
4. **Advanced Model Tuning**: Apply hyperparameter tuning and ensemble methods.

## Installation and Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/FransDroid/flight_delays_predict.git
   cd flight-delay-prediction
