# 🌧️ Advanced Techniques for Accurate Precipitation Forecasting

## 📌 Project Overview  
This project explores **Deep Learning-based techniques** for **accurate precipitation forecasting**. Weather prediction is crucial for various industries, including **agriculture, transportation, energy, and disaster management**. Traditional forecasting models often struggle with accuracy due to the complexity of atmospheric interactions.  

To address this challenge, our project leverages **Deep Learning models**, including **Recurrent Neural Networks (RNNs), Long Short-Term Memory (LSTM) networks, and Artificial Neural Networks (ANNs)**, to **predict precipitation using historical weather data**.  

## 🎯 Objectives  
- Develop a **highly accurate precipitation forecasting system**.  
- Utilize **Deep Learning techniques** to capture temporal dependencies in weather data.  
- Enhance **resource management and disaster preparedness** with better forecasting.  

## 🔬 Dataset  
- **Source:** [Sri Lanka Weather Dataset](https://www.kaggle.com/datasets/rasulmah/sri-lanka-weather-dataset)  
- **Duration:** January 1, 2010 – January 1, 2023  
- **Features Included:**  
  - Temperature (Max, Min, Mean)  
  - Apparent Temperature  
  - Wind Speed, Wind Gusts, Wind Direction  
  - Precipitation & Precipitation Hours  
  - Shortwave Radiation & Solar Energy Input  
  - Evapotranspiration (ET0)  
  - Geographic Data (Latitude, Longitude, Elevation)  

## 🛠️ Tech Stack  
### **Machine Learning & Deep Learning Models:**  
- **Long Short-Term Memory (LSTM)** – Primary model for time-series prediction  
- **Artificial Neural Networks (ANNs)** – For non-sequential data processing  
- **Recurrent Neural Networks (RNNs)** – Captures sequential dependencies  

### **Development Tools & Libraries:**  
- **Python**  
- **TensorFlow / Keras**  
- **scikit-learn**  
- **NumPy & Pandas**  
- **Matplotlib & Seaborn**  

## ⚙️ Data Preprocessing  
1. **Feature Engineering:**  
   - Convert timestamps to datetime format  
   - Create new features (Year, Month)  
   - Drop irrelevant columns (e.g., `weather_code`)  
2. **Handling Missing Data:**  
   - Replace zero values with mean  
   - Detect and remove outliers using **Interquartile Range (IQR)**  
3. **Data Normalization:**  
   - **MinMaxScaler** applied to scale features between [0,1]  
4. **Splitting the Dataset:**  
   - **Training (80%)** and **Testing (20%)** sets  
   - Sequence generation with a 30-day sliding window  

## 🏗️ Model Architecture  
### **1️⃣ LSTM Model (Best Performing)**
- 2 LSTM Layers (100 & 50 units)  
- Fully Connected (Dense) Layer (50 neurons, ReLU)  
- Output Layer (Single neuron for regression)  
- **Mean Squared Error (MSE):** **2.88**  
- **R² Score:** **0.797**  

### **2️⃣ ANN Model**
- 3 Hidden Layers (256, 128, 32 neurons)  
- ReLU Activation & Dropout (30%)  
- **MSE:** 3.26 | **R² Score:** 0.770  

### **3️⃣ RNN Model**
- 1 Simple RNN Layer (50 units, tanh activation)  
- Dense Output Layer (Linear activation)  
- **MSE:** 0.0377 | **R² Score:** 0.151  

## 📊 Results & Performance Comparison  
| Model | MSE (Lower is Better) | R² Score (Higher is Better) |
|--------|-----------------|------------|
| **LSTM** (Best) | 2.88 | **0.797** |
| ANN | 3.26 | 0.770 |
| RNN | 0.0377 | 0.151 |

### 🏆 **Why LSTM?**
✔️ Best accuracy for precipitation prediction.  
✔️ Handles **long-term dependencies** in weather data.  
✔️ **Captures complex temporal patterns** effectively.  

### 👨‍💻 Contributors
- Wijekulasuriya E.G.C.S – Data Preprocessing & Model Implementation
- Fernando W.Y.M – Data Handling & ANN Model
- Gunasekara W.M.W.A.G.T.N.A – Feature Engineering & Evaluation
- Mahawaththa N.T.M.A.S.M – LSTM Implementation & Optimization
