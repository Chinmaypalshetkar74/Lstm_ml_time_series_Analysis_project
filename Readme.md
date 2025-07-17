⚡ LSTM-Based Time Series Forecasting for Energy Consumption

This project applies Deep Learning—specifically LSTM (Long Short-Term Memory) networks—for time series forecasting of energy consumption data. The model is trained to predict daily electricity consumption based on historical usage data. It is inspired by Mohamad Nachawati’s open project and thesis.


---

📌 Project Objective

To develop an LSTM-based deep learning model capable of predicting daily energy consumption using historical time series data. The prediction model is focused on aiding:

Smart energy planning

Renewable energy optimization

Load balancing and infrastructure efficiency



---

📊 Dataset

Source: Finland's electricity consumption data (2016–2021)

Format: Hourly time series data

Features Used: DateTime and Energy Consumption (MWh)



---

🧠 Techniques & Tools

Category	Tools/Methods

Data Preprocessing	Pandas, NumPy, MinMaxScaler
Visualization	Matplotlib, Seaborn
Deep Learning	TensorFlow/Keras
Model	Stacked LSTM with 4 layers and Dropout
Evaluation	Root Mean Square Error (RMSE)



---

🔄 Workflow Overview

1. Load and explore dataset
2. Clean and preprocess the time series data
3. Resample hourly data to daily mean values
4. Normalize data using MinMaxScaler
5. Split into training, validation, and testing sets
6. Reshape data to 3D for LSTM input: [samples, time_steps, features]
7. Build a stacked LSTM model with Dropout
8. Train the model and evaluate with RMSE
9. Visualize predictions vs actual consumption


---

🧪 Model Architecture

Input Shape: (samples, 100 time steps, 1 feature)

Layers:

4 LSTM Layers (50 units each)

Dropout Layer (20%)

Dense Output Layer


Optimizer: Adam

Loss Function: Mean Squared Error

Metric: Root Mean Square Error (RMSE)



---

📈 Results

The model performs well on short-term energy prediction, especially for daily consumption patterns. Accuracy varies depending on the chosen time_step window size

✅ Demonstrates LSTM's strength in handling seasonality and trend in univariate time series
