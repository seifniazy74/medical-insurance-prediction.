# Medical Insurance Cost Prediction Project

## 📌 Project Overview
This project aims to **predict medical insurance charges** based on demographic and health-related features using machine learning models.  
The dataset contains information about individuals, including their **age, sex, BMI, number of children, smoking status, and region**.  
The **target variable** is the insurance charges.

---

## 📊 Data Description
- **age**: Age of the individual *(integer)*
- **sex**: Gender of the individual *(male/female)*
- **bmi**: Body Mass Index *(float)*
- **children**: Number of children/dependents *(integer)*
- **smoker**: Smoking status *(yes/no)*
- **region**: Residential area *(southeast, southwest, northeast, northwest)*
- **charges**: Medical insurance cost *(float, target variable)*

✅ The dataset is clean, with **no missing values**.  
✅ Categorical features are encoded using **LabelEncoder** for model compatibility.  

---

## 🔎 Data Analysis & Visualization
- **Distribution plots & boxplots** → Understand spread & detect outliers in numerical features.
- **Count plots & value counts** → Visualize distribution of categorical features.
- **Outliers** in `bmi` and `charges` were handled using the **IQR method**.

---

## 🛠️ Data Preprocessing
- Categorical variables (`sex`, `smoker`, `region`) were **encoded**.  
- Outliers were **capped** using IQR.  
- Features and target were split into **X and y**.  
- Data was split into **training and testing sets (80/20 split)**.  
- Numerical features were scaled using **RobustScaler**.  

---

## 🤖 Model Training & Evaluation
Two models were trained and evaluated:

### 1️⃣ Linear Regression
- Trained on processed data.  
- Evaluated with:
  - **Mean Squared Error (MSE)**
  - **Mean Absolute Error (MAE)**
  - **R² score**

### 2️⃣ Random Forest Regressor
- An **ensemble regression model**.  
- Evaluated with the same metrics.  
- Usually **performs better** because it captures **non-linear relationships**.  

---

## 📈 Results
- Both models were tested on the test set.  
- **Evaluation metrics (MSE, MAE, R²)** were compared.  
- **Random Forest** showed **better performance** overall.  

---

## 🖥️ Prediction System
A **simple prediction system** was built to estimate insurance charges for new input data:  
- Input features are **encoded**.  
- Passed into the **trained model**.  
- Output = **Predicted insurance charges**.  

---

## 📂 Data Explanation
- **age** → Ranges from young adults to seniors.  
- **sex** → Male or female.  
- **bmi** → Higher values may indicate overweight/obesity.  
- **children** → Number of dependents covered.  
- **smoker** → Strongly impacts charges.  
- **region** → Regional differences in costs.  
- **charges** → Target variable (actual insurance cost).  

---

## 🔑 Key Points
- ✅ No missing values → Dataset is complete.  
- ✅ Categorical encoding → `sex`, `smoker`, `region` encoded numerically.  
- ✅ Outliers handled in `bmi` and `charges`.  
- ✅ Most important features: **Age, BMI, Smoking Status**.  

---

## 🎯 Conclusion
This dataset is suitable for **regression analysis** and demonstrates how **demographic and lifestyle factors impact medical insurance costs**.
