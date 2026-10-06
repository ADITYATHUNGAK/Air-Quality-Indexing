Air Quality Monitoring and Forecasting System:
Link: https://jj4szpruvbeuxzfnuldiy7.streamlit.app/
1.Overview:

This project is an end-to-end Internet of Things (IoT)–based Air Quality Monitoring and Forecasting system. It combines embedded hardware, cloud computing, data visualisation, and machine learning to monitor environmental conditions and predict short-term air quality trends.
An ESP32 microcontroller programmed using MicroPython collects sensor data and transmits it to the Supabase cloud platform. A Streamlit dashboard developed in Python visualises live, historical, and forecasted data. A machine learning model based on XGBoost regression forecasts Air Quality Index (AQI) values for the next one hour at ten-minute intervals.
-----------------------------------------------------------------------------------

2.System Workflow:

1.Sensors connected to the ESP32 measure air quality parameters.
2.The ESP32 sends sensor data to Supabase using Wi-Fi.
3.Supabase stores data with timestamps for real-time and historical access.
4.The Streamlit application retrieves data from Supabase.
5.The machine learning model forecasts AQI values and displays results on the dashboard.
--------------------------------------------------------------------------------------

3.Hardware Components:

1.ESP32 microcontroller (MicroPython)
2.MQ-2 gas sensor
3.DHT22 temperature and humidity sensor
4.Dust sensor
5.Breadboard, jumper wires, and power supply
------------------------------------------------------------------------------------------------

4.Software Stack:

1.MicroPython – Firmware development for ESP32
2.Supabase – Cloud database and backend services
3.Python – Data processing and machine learning
4.Streamlit – Web-based dashboard
5.XGBoost – AQI prediction model
6.Pandas, NumPy – Data analysis
7.Matplotlib / Plotly – Data visualisation
----------------------------------------------------------------------------------------------------

5.Dashboard Features:

Live Data: Displays real-time AQI, temperature, humidity, and dust concentration values received from the ESP32.
Historical Data: Provides visualisations of previously stored data to analyse trends and pollution patterns.
Future Data: Shows predicted AQI values for the next one hour at ten-minute intervals.
Machine Learning Model: The AQI forecasting module uses an XGBoost regression model trained on historical AQI data. To avoid incorrect or unstable predictions, the model uses only the most recent thirty minutes of AQI data as input. This rolling window approach ensures predictions are based on current environmental conditions and reduces the influence of outdated or noisy sensor readings.The trained model is stored as a serialized .joblib file and loaded dynamically for real-time prediction.
---------------------------------------------------------------------------------------------------------

6.Project Structure:

├── devices/
├── .gitignore
├── app.py
├── aqi_six_models.joblib
├── README.md
├── requirements.txt
------------------------------------------------------------------------------------------------------------------

7.Applications:

1.Air quality monitoring systems
2.Smart city infrastructure
3.Environmental research projects
4.Academic and student projects
----------------------------------------------------------------------------------------------------------------

10.Author:
Aditya Thunga K
