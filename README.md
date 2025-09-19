# 🎬 Predicting Movie Rental Durations  

![DVD Image](dvd_image.jpg)  

A DVD rental company needs your help! They want to figure out how many days a customer will rent a DVD for based on available features.  
The company aims to optimize **inventory planning** by using regression models to predict rental durations, with the goal of achieving an **MSE ≤ 3** on the test set.  

---

## 📌 Guiding Questions  
- How many days will a customer rent a DVD?  
- Which features provide the strongest predictive power?  
- What regression model performs best with the lowest mean squared error?  

---

## 📂 The Data  

**`rental_info.csv`** — contains customer rental data with the following features:  

- `rental_date`: The date/time the DVD was rented.  
- `return_date`: The date/time the DVD was returned.  
- `amount`: Amount paid for renting the DVD.  
- `amount_2`: Square of `amount`.  
- `rental_rate`: Rental rate for the DVD.  
- `rental_rate_2`: Square of `rental_rate`.  
- `release_year`: Year the movie was released.  
- `length`: Length of the movie (minutes).  
- `length_2`: Square of `length`.  
- `replacement_cost`: Replacement cost of the DVD.  
- `special_features`: Special DVD features (e.g., trailers, deleted scenes).  
- `NC-17`, `PG`, `PG-13`, `R`: Dummy variables for movie ratings.  

---

## 🛠️ Project Steps  

### 1. Getting Rental Length  
- Converted `rental_date` and `return_date` into datetime.  
- Created `rental_length_days` column for target variable.  

### 2. Feature Engineering  
- Added dummy variables for `special_features` → `deleted_scenes`, `behind_the_scenes`.  
- Built feature set `X` and target `y` (`rental_length_days`).  

### 3. Train-Test Split  
- Split dataset into train (80%) and test (20%).  
- Used `random_state=9` for reproducibility.  

### 4. Feature Selection  
- Applied **Lasso Regression** for identifying strong predictors.  

### 5. Model Training & Tuning  
- Tested multiple regression models.  
- Performed hyperparameter tuning to optimize performance.  

### 6. Model Evaluation  
- Predicted rental durations on the test set.  
- Evaluated performance using **Mean Squared Error (MSE)**.  

### 7. Best Model  
- Recommended best-performing regression model with **MSE < 3**.  
- Stored as `best_model` and score as `best_mse`.  

---

## ✅ Key Deliverables  
- Engineered rental duration feature from datetime columns.  
- Created dummy variables for categorical features.  
- Implemented multiple regression models with hyperparameter tuning.  
- Selected best-performing model with **MSE < 3** on test set.  
- Provided actionable insights for **DVD inventory optimization**.  

---

## 🧰 Skills Used  
- Python (`pandas`, `numpy`, `scikit-learn`)  
- Regression modeling (linear, lasso, ridge)  
- Feature engineering & preprocessing  
- Train-test split & evaluation  
- Mean Squared Error (MSE) for regression metrics  
