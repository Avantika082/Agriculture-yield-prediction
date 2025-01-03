# Agricultural Yield Prediction using LightGBM

## Project Overview
This project focuses on predicting agricultural crop yields using ensemble learning techniques, specifically leveraging the **LightGBM** boosting framework. The dataset includes features such as **average rainfall**, **average temperature**, and **pesticide usage**, which are crucial in determining crop productivity. By using a robust machine learning approach, this project aims to aid in forecasting crop yields effectively, benefiting farmers, policymakers, and the agriculture industry.

---

## Objectives
- **Predict Crop Yield:** Develop a predictive model for agricultural yield based on environmental and input variables.
- **Use Ensemble Learning:** Implement LightGBM, a gradient boosting algorithm, for improved accuracy and performance.
- **Feature Impact Analysis:** Analyze the influence of factors such as rainfall, temperature, and pesticide usage on crop yield.

---

## Dataset
The dataset used for this project contains the following columns:
- **Area:** Geographical region of crop production.
- **Year:** Year of observation.
- **Item:** Type of crop.
- **Yield:** Crop yield (target variable).
- **Average Rainfall (mm):** Average annual rainfall in millimeters.
- **Average Temperature (°C):** Average annual temperature in degrees Celsius.
- **Pesticides (tonnes):** Annual pesticide usage in tonnes.

---

## Methodology
### 1. Data Preprocessing
- Clean and handle missing values in the dataset.
- Normalize or scale numerical features as required.
- Encode categorical features (if applicable) using one-hot or label encoding.

### 2. Feature Engineering
- Analyze and select the most relevant features for prediction.
- Engineer new features if necessary (e.g., rainfall-to-temperature ratio).

### 3. Model Implementation
- Use **LightGBM** for regression:
  - Objective: Regression
  - Metric: Root Mean Squared Error (RMSE)
  - Boosting Type: Gradient Boosting Decision Trees (GBDT)
- Hyperparameters:
  - `num_leaves`: 31
  - `learning_rate`: 0.05
  - `feature_fraction`: 0.8
  - `num_boost_round`: 200
  - `early_stopping_rounds`: 10

### 4. Model Training
- Split the dataset into training and testing sets.
- Train the LightGBM model using the training data and validate using the testing data.
- Monitor RMSE during training for performance evaluation.

### 5. Evaluation
- Evaluate the model using metrics such as RMSE and Mean Squared Error (MSE).
- Compare predicted vs actual crop yields using visualization techniques.

---

## Installation
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the project:
   ```bash
   python main.py
   ```

---

## Results
- **Performance:** The LightGBM model achieved an RMSE of `X.XX` on the test dataset.
- **Insights:**
  - **Rainfall:** Significant correlation with crop yield.
  - **Temperature:** Moderate effect on crop yield.
  - **Pesticides:** Minimal but non-negligible impact on yield.

---

## Visualizations
The following visualizations were created:
1. **Feature Correlations:** Heatmap showing relationships between rainfall, temperature, pesticide usage, and crop yield.
2. **Predicted vs Actual Yields:** Scatter plot to visualize model accuracy.
3. **Feature Importance:** Bar chart showing LightGBM feature importance scores.

---

## Future Improvements
- Incorporate additional features like soil type, fertilizer usage, and irrigation methods.
- Use more advanced ensemble learning techniques for further performance gains.
- Extend the model to predict yields for multiple crops simultaneously.

---

## License
This project is licensed under the MIT License.

---

## Acknowledgments
- The dataset was sourced from [Kaggle](https://www.kaggle.com) and similar repositories.
- Thanks to the developers of LightGBM for creating an efficient boosting framework.
- Special thanks to the contributors of open-source libraries used in this project.

---



