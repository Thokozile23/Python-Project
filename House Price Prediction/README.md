# 🏠 House Price Prediction: Machine Learning Project

Welcome to the **House Price Prediction** project! This repository demonstrates how to use machine learning to predict housing prices based on demographic and geographic features. Using various machine learning models, I compared their performance to identify the best approach for this task.

---

## 📊 Project Overview
This project focuses on predicting the **median house value** in California using the **California Housing Dataset**. I:

1. Performed **exploratory data analysis (EDA)** to uncover key correlations.
2. Used **feature engineering** to enhance the dataset.
3. Trained and evaluated **linear regression** and **random forest regressor** models.
4. Fine-tuned the random forest model using **GridSearchCV**.

---

## 🛠️ Tools and Libraries Used
- **Python**: Main programming language.
- **Libraries**:
  - **Pandas**: Data manipulation.
  - **NumPy**: Numerical operations.
  - **Matplotlib & Seaborn**: Data visualization.
  - **scikit-learn**: Machine learning models and tools.
  - **Jupyter Notebook**: Interactive environment for code execution.

---

## 🔄 Steps in the Project

### 1. **🔄 Data Preprocessing**
- Imported and cleaned the California housing dataset.
- Transformed features using **log transformations** to reduce skewness in variables such as:
  - Total rooms
  - Total bedrooms
  - Population
  - Households
- Applied **one-hot encoding** to the `ocean_proximity` categorical variable.

### 2. **✨ Feature Engineering**
- Created new features to improve predictive performance:
  - `bedroom_ratio`: Ratio of total bedrooms to total rooms.
  - `household_rooms`: Ratio of total rooms to households.
- Observed the following correlations:
  - **📊 Strong positive correlation** between median income and median house value.
  - **🔻 Negative correlation** between longitude and latitude.
  - **🔻 Negative correlation** between bedroom ratio and median house value.
  - **📊 Weak positive correlation** between household rooms and median house value.

### 3. **🔍 Exploratory Data Analysis (EDA)**
- Visualized data trends using **scatter plots, histograms, and heatmaps**.
- Identified that most expensive houses were located near the coastline.

### 4. **💡 Model Training**
- **Linear Regression**:
  - Trained using `scikit-learn`'s `LinearRegression()`.
  - Achieved a score of **0.685**.
- **Random Forest Regressor**:
  - Trained using `RandomForestRegressor()`.
  - Achieved a score of **0.825**.

### 5. **🔧 Hyperparameter Tuning**
- Used **GridSearchCV** to fine-tune the random forest model.
- Hyperparameters optimized:
  - Number of estimators: `[100, 200, 300]`
  - Minimum samples split: `[2, 4]`
  - Maximum depth: `[None, 4, 8]`
- Best model achieved a score of **0.824**.

### 6. **📊 Model Evaluation**
- **Tested models** on unseen test data using R-squared as the evaluation metric.
- Random forest performed the best, explaining **82.5% of the variance** in the test data.

---

## 📊 Results
| Model                  | R-Squared Score |
|------------------------|-----------------|
| Linear Regression      | 0.685           |
| Random Forest Regressor| 0.825           |
| Tuned Random Forest    | 0.824           |

---

## 📊 Visualizations
### Correlation Heatmap
🎨 ![](images/correlation_heatmap.png)

### Feature Importance (Random Forest)
🎨 ![](images/feature_importance.png)

---

## 🔍 Key Takeaways
- **Income is the strongest predictor** of house prices.
- Longitude and latitude show a geographical price trend.
- Features like bedroom ratio and household rooms provide additional insights into pricing dynamics.

---

## 🛠️ How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/username/house-price-prediction.git
   ```
2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook to reproduce results:
   ```bash
   jupyter notebook HousePricePrediction.ipynb
   ```

---

## 🔗 Future Work
- Incorporate more advanced models like Gradient Boosting and XGBoost.
- Explore additional features to improve predictive power.
- Deploy the model as a web application for real-time predictions.

---

## 👨‍💻 Author
**Thokozile Munthali**  
Feel free to reach out for questions or collaboration!
To highlight your email and LinkedIn URL effectively, you can use bold formatting, color coding, or clickable links. Here's an example:

✉ **[thokomunthali22@gmail.com](mailto:thokomunthali22@gmail.com)**  
🔗 **[LinkedIn Profile](https://www.linkedin.com/in/thokozile-munthali/)**  



