# Fight-Fare-Prediction
ML-based Ticket Price Estimation

# Flight Fare Predictor: ML-based Ticket Price Estimation

## Project Overview

This project aims to predict the price of flight tickets based on various features like airline, source and destination cities, departure time, stops, class, and days left before departure. The dataset used contains approximately **300,000 records with 11 attributes**. Through exploratory data analysis (EDA), feature engineering, and machine learning models, this project provides insights into flight pricing patterns and builds predictive models for price estimation.

---

## Dataset Information

The dataset contains flight booking records with the following attributes:

```
| Column Name      | Description                                      |
|------------------|--------------------------------------------------|
| Airline         | Name of the airline company                      |
| Flight         | Flight code of the plane                         |
| Source City     | City from which the flight takes off            |
| Departure Time  | Time of departure                               |
| Stops          | Number of stops between source and destination  |
| Arrival Time    | Time of arrival                                 |
| Destination City| City where the flight lands                    |
| Class          | Seat class (Economy, Business)                  |
| Duration       | Total travel time in hours                      |
| Days Left      | Difference between booking date and travel date |
| Price         | Ticket price (Target variable)                   |
```

---

## Tasks Performed

### 1. Data Preprocessing
   - Loaded the dataset and removed unnecessary columns.
   - Checked for missing values and handled them appropriately.
   - Converted categorical variables using **One-Hot Encoding**.
   - Performed feature selection using **Variance Inflation Factor (VIF)** to remove multicollinear features.

### 2. Exploratory Data Analysis (EDA)
   - Visualized the distribution of flight prices.
   - Analyzed the relationship between flight price and factors such as:
     - Airlines
     - Days left before departure
     - Seat class (Economy vs. Business)
     - Source and destination cities
   - Used **count plots** to visualize categorical features.

### 3. Feature Selection
   - Used **correlation matrix** to identify important features.
   - Applied **VIF (Variance Inflation Factor)** to drop redundant features (e.g., the "Stops" feature).

### 4. Machine Learning Models Implemented
   - **Linear Regression**
     - Standardized the data before training.
     - Model evaluation:
       - **RMSE**: 7259.93
       - **MAPE**: 34%
     - Lower RMSE and MAPE indicate better model performance.

   - **Decision Tree Regressor**
     - Model evaluation:
       - **RMSE**: 3620
       - **MAPE**: 7.7%
     - Outperformed the Linear Regression model.

   - **Random Forest Regressor**
     - Model evaluation:
       - **RMSE**: 2824
       - **MAPE**: 7.3%
     - Performed the best among all models.

---

## Results & Findings

- Flight ticket prices **increase as the departure date gets closer**.
- Business class tickets are significantly more expensive than economy class.
- Certain airlines consistently have higher prices.
- **Random Forest Regressor** provided the most accurate predictions with the lowest RMSE and MAPE.

---

## Installation & Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/flight-fare-predictor.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook to explore the dataset and train models.

---

## Future Improvements

- Experiment with **deep learning models** such as neural networks for price prediction.
- Incorporate **real-time flight data** for dynamic pricing predictions.
- Enhance feature engineering by considering additional variables like **seasonality and holidays**.

---

