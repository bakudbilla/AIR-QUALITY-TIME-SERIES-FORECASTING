# AIR-QUALITY-TIME-SERIES-FORECASTING

This project forecasts PM2.5 air pollution levels using time-series data and deep learning techniques, specifically LSTM and Bidirectional LSTM layers.

---

## 1. Data Exploration & Cleaning

- Handled missing values and outliers  
- Visualized data distributions for deeper insights  

## 2. Feature Engineering

- Extracted time-based features from the datetime column:
  - Hour
  - Day
  - Month
  - Weekday  

## 3. Data Normalization

- Standardized input features to enhance model convergence and accuracy  

## 4. Model Building

- Built a deep learning model using:
  - Stacked LSTM layers
  - Bidirectional LSTM for better context capture  

## 5. Training & Evaluation

- Split the data into training and validation sets  
- Evaluated model performance using:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)  

## 6. Prediction Output

- Generated final predictions on the test set  
- Saved output files for submission  

---

## Model Architecture

| Layer               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Layer Normalization | Stabilizes training by normalizing activations across features             |
| LSTM (64 units)     | Sequence modeling layer with ReLU activation and regularization            |
| Layer Normalization | Further stabilizes learning post-LSTM                                      |
| Dropout (30%)       | Prevents overfitting by randomly dropping neurons during training          |
| LSTM (32 units)     | Final LSTM layer, `return_sequences=False`, uses ReLU and regularization   |
| Dropout (20%)       | Additional regularization to improve generalization                        |
| Dense (64 units)    | Fully connected layer with ReLU and L2 regularization                       |
| Dropout (20%)       | Final dropout before prediction                                             |
| Output (1 unit)     | Predicts final PM2.5 value as a continuous output                           |

---

## Dataset

- **Train Data:** `train.csv`  
  - 30,676 rows × 12 columns  
  - Includes datetime, meteorological variables, and target `pm2.5`

- **Test Data:** `test.csv`  
  - 13,148 rows × 11 columns  
  - Contains the same features as training data, excluding `pm2.5`  

---

## Prerequisites

- Python 3.7+
- Required libraries:
  - pandas  
  - numpy  
  - seaborn  
  - matplotlib  
  - scikit-learn  
  - tensorflow  

---

## Project Structure
```
├── data/
│   ├── train.csv
│   └── test.csv
├── notebooks/
│   └── Air_Quality_Forecasting_Best_model.ipynb
├── outputs/
│   ├── subm_fixed_1.csv
│   ├── subm_fixed_2.csv
│   ├── subm_fixed_3.csv
│   ├── subm_fixed_4.csv
│   ├── subm_fixed_5.csv
│   ├── subm_fixed_6.csv
│   ├── subm_fixed_7.csv
│   ├── subm_fixed_8.csv
│   ├── subm_fixed_9.csv
│   ├── subm_fixed_10.csv
│   ├── subm_fixed_11.csv
│   ├── subm_fixed_12.csv
│   ├── subm_fixed_13.csv
│   ├── subm_fixed_14.csv
│   ├── subm_fixed_15.csv
│   ├── subm_fixed_16.csv
│   └── subm_fixed_17.csv
│   └── subm_fixed_18.csv
│   └── subm_fixed_19.csv
└── README.md
```
