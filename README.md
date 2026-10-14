# Household Electricity Consumption Prediction Using GRU

## Overview
This project uses a Gated Recurrent Unit (GRU) deep learning model to predict household electricity consumption from historical electricity measurements.

## Objective
To learn temporal patterns in household electricity usage and predict the next Global Active Power reading.

## Dataset
The project uses the Household Electric Power Consumption dataset.

Seven features are used:
- Global Active Power
- Global Reactive Power
- Voltage
- Global Intensity
- Sub-metering 1
- Sub-metering 2
- Sub-metering 3

The dataset is cleaned, sorted chronologically, and prepared for time-series forecasting. The model was developed using 50,000 valid records.

## Model Architecture
- GRU layer with 64 units
- Dropout layer with a rate of 0.2
- Dense layer with 16 neurons and ReLU activation
- Dense output layer for the prediction

The model uses the previous 120 readings to predict the next Global Active Power value.

## Training
- Optimizer: Adam
- Loss function: Mean Squared Error (MSE)
- Evaluation metrics: Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE)
- Data split: 70% training, 15% validation, and 15% testing

## Test Results

| Metric | GRU Model |
|---|---:|
| MAE | 0.1686 kW |
| RMSE | 0.3554 kW |

A persistence baseline was also evaluated for comparison. The GRU achieved a lower RMSE, while the baseline achieved a lower MAE.

## Technologies Used
- Python
- Jupyter Notebook
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras

## How to Run
1. Clone or download this repository.
2. Install the required Python libraries.
3. Open `Household_Electricity_Prediction.ipynb` in Jupyter Notebook.
4. Update the dataset path to the location on your computer.
5. Run the notebook cells in order.

## Limitations
Prediction accuracy may vary across different time periods. The model's performance should be compared with simple baselines and evaluated on additional unseen data.

## Future Improvements
- Improve forecasting accuracy.
- Evaluate different sequence lengths and model architectures.
- Build an interactive prediction interface.
- Explore longer-term electricity demand forecasting.

## Author
Adharsh
