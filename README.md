# 🚀 Solar Wind Data Analysis and Prediction

This project analyzes a dataset of solar wind parameters to predict solar wind speed using various machine learning models. This work was completed as part of my internship at the Dhee Centre for AI and Data Science.

## 📄 Problem Statement

Solar wind can disrupt critical infrastructure like satellites and power grids. However, current methods for predicting solar wind conditions are often not reliable enough. The goal of this project is to analyze historical solar wind data and build machine learning models to provide more accurate predictions of its parameters, focusing on solar wind speed.

## ✨ Key Accomplishments

* **Data Cleaning:** Successfully identified and handled erroneous data points (marked as -99999) through a robust preprocessing pipeline using Pandas.
* **Exploratory Data Analysis (EDA):** Performed in-depth statistical and visual analysis to uncover key trends, distributions, and correlations within the data, such as a strong positive correlation of **0.81** between wind speed and temperature.
* **Model Comparison:** Implemented, trained, and evaluated four different regression models to determine the most effective approach for predicting solar wind speed.
* **Performance Evaluation:** Quantified model performance using MAE and RMSE metrics, identifying **Random Forest** as the most accurate model with an **RMSE of 12.95**.

## ⚙️ Technologies Used

* **Language:** Python
* **Libraries:**
    * Pandas & NumPy (Data Manipulation)
    * Matplotlib & Seaborn (Data Visualization)
    * Scikit-learn (Machine Learning)
    * Jupyter Notebook (Development Environment)

## 📊 Methodology

The project followed a structured data science workflow:

### 1. Data Cleaning and Preprocessing

* The initial dataset contained **1635** records with numerous features like magnetic field strength, particle density, speed, and temperature.
* A preliminary statistical analysis revealed extreme outliers (e.g., -99999 values), indicating missing or faulty sensor readings.
* A filtering process was applied to remove these records, resulting in a clean dataset of **1211** high-quality data points for analysis and modeling.

### 2. Exploratory Data Analysis (EDA)

* **Histograms and Box Plots** were generated to visualize the distribution of key parameters like magnetic field (`Bt-med`), density (`Dens-med`), speed (`Speed-med`), and temperature (`Temp-med`).
* A **Correlation Heatmap** was created to identify relationships between variables. This revealed a strong positive correlation of **0.81** between `Speed-med` and `Temp-med`.
* **Scatter Plots** were used to further investigate the relationships between the most correlated features.

### 3. Machine Learning and Prediction

* The prediction target was set to `Speed-med` (median solar wind speed).
* The data was split into an 80% training set and a 20% testing set.
* Features were standardized using `StandardScaler` to ensure optimal performance for all models.
* Four regression models were trained and evaluated:
    1.  Linear Regression
    2.  Polynomial Regression (Degree 2)
    3.  Random Forest Regressor
    4.  Gradient Boosting Regressor

## 📈 Results

The performance of each model was evaluated using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE). The Random Forest model demonstrated the best performance.

| Model                       | MAE     | RMSE    |
| --------------------------- | ------- | ------- |
| Linear Regression           | 12.56   | 18.81   |
| Polynomial Regression (Deg 2) | 10.44   | 14.69   |
| Gradient Boosting           | 9.67    | 13.57   |
| **Random Forest** | **8.85** | **12.95** |

*All result values are cited from the source notebook.*

**Conclusion:** The Random Forest Regressor is the most effective model for this prediction task, achieving the lowest error rates.

## 🚀 How to Run this Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd your-repo-name
    ```
3.  **Install the required libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn jupyter
    ```
4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
5.  Open the `solar wind data analysis-Copy2.ipynb` file to view and run the code.
