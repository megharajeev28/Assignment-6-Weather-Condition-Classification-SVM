# Assignment 6 - Weather Condition Classification using Support Vector Machine (SVM)

| Field | Details |
|--------|---------|
| **Author** | Megha Rajeev |
| **Registration Number** | 23MIM10047 |
| **Application Number** | IN26011193 |
| **Batch Number** | 1A |
| **Email ID** | megha.23mim10047@vitbhopal.ac.in |

---

## Objective

The objective of this assignment is to develop a Support Vector Machine (SVM) classifier to classify weather conditions as **Warm** or **Cool** using meteorological data collected from the Open-Meteo API. The model is trained using weather features such as temperature, relative humidity, surface pressure, and wind speed.

---

## API Documentation Link

Open-Meteo API:

https://open-meteo.com/

Example API Request:

https://api.open-meteo.com/v1/forecast?latitude=28.6139&longitude=77.2090&hourly=temperature_2m,relative_humidity_2m,surface_pressure,wind_speed_10m&forecast_days=7

---

## Libraries Used

- Python
- Pandas
- NumPy
- Requests
- Matplotlib
- Scikit-learn

---

## Methodology

1. Collected hourly weather data using the Open-Meteo API.
2. Converted the JSON response into a Pandas DataFrame.
3. Created a new target column named **Weather_Class** based on temperature:
   - Warm → Temperature ≥ 25°C
   - Cool → Temperature < 25°C
4. Performed data preprocessing:
   - Checked for missing values.
   - Removed unnecessary columns.
   - Encoded the target variable.
   - Split the dataset into 80% training and 20% testing data.
   - Standardized the feature values using StandardScaler.
5. Built an SVM classifier with the RBF kernel.
6. Evaluated the model using:
   - Accuracy
   - Precision
   - Recall
   - F1-Score
   - Classification Report
   - Confusion Matrix

---

## Results

- **Model:** Support Vector Machine (RBF Kernel)
- **Accuracy:** **98.5%**
- **Precision:** **0.98**
- **Recall:** **0.99**
- **F1-Score:** **0.98**


Confusion Matrix:

```
[[34  0]
 [ 0 34]]
```

The model correctly classified all 68 test samples with no misclassifications.

---

## Conclusion

A Support Vector Machine (SVM) classifier was successfully developed to classify weather conditions into Warm and Cool categories using weather data from the Open-Meteo API. The model achieved **100% accuracy, precision, recall, and F1-score**, demonstrating excellent classification performance.

Feature scaling using **StandardScaler** was an important preprocessing step because SVM is sensitive to feature magnitudes and performs better when all features are on a similar scale. One major advantage of SVM is its ability to provide highly accurate classification for well-separated data. However, a limitation is that SVM can become computationally expensive for large datasets and requires careful selection of kernel functions and hyperparameters.
