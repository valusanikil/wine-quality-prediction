# Wine Quality Prediction – Precision in Every Sip

## Overview

Wine quality prediction is critical for wineries in a competitive market where consumers demand high-quality wines at competitive prices. This project uses the physicochemical properties of wine samples to predict quality and offer recommendations to improve consistency and quality.

---

## Business Problem

- **Competitive Landscape:**  
  The wine industry faces fierce competition from both domestic and international producers.
  
- **Consumer Demands:**  
  Consumers expect wines that deliver high quality at a reasonable price.
  
- **Consistency Requirement:**  
  Wineries need robust methods to ensure consistent high-quality production to maintain competitiveness.

---

## Prior Research and Methodology

- **Classification vs. Regression:**  
  Previous studies have explored both regression and classification techniques. A common approach is to convert continuous quality scores into binary categories (e.g., “good” vs. “not good”) using a cutoff (often a quality score of 7 or higher).
  
- **Data Transformation:**  
  Transforming quality scores into categorical outcomes simplifies modeling with many machine learning algorithms.
  
- **Workflow:**  
  The process includes:
  - **Data Reading & Exploratory Data Analysis (EDA)**
  - **Data Transformation & Feature Selection**
  - **Train-Test Splitting**
  - **Modeling (e.g., Decision Trees)**
  - **Performance Evaluation (using ROC curves, accuracy, etc.)**

- **Citation:**  
  Our work builds on research such as:  
  *P. Cortez, A. Cerdeira, F. Almeida, T. Matos, and J. Reis, “Modeling wine preferences by data mining from physicochemical properties,” Decision Support Systems, Elsevier, 47(4):547-553, 2009.*

---

## Data

Two datasets are used in this project:

- **Red Wine Dataset:**  
  Contains physicochemical properties and quality scores for red wine samples.
  
- **White Wine Dataset:**  
  Contains similar measurements for white wine samples.

**Data Integration:**  
- The datasets are merged by adding an extra column that indicates the type of wine (red or white).  
- The final dataset consists of 11 feature variables (e.g., fixed acidity, volatile acidity, citric acid, etc.) and the target variable (quality).

---

## Models Evaluated

The following machine learning models were applied:

- **Random Forest Classifier**
- **Logistic Regression**
- **Linear Discriminant Analysis**
- **k-Nearest Neighbors (KNN)**
- **Decision Tree Classifier**
- **Naive Bayes**
- **Support Vector Machine (SVM)**

Models were compared using performance metrics to determine the best approach for predicting wine quality.

---

## Process and Workflow

1. **Data Collection & Reading:**  
   - Import red and white wine datasets.  
   - Add a column indicating wine type.
   
2. **Exploratory Data Analysis (EDA):**  
   - Check for missing values and analyze basic statistics.  
   - Visualize distributions (e.g., histograms) and relationships (e.g., correlation plots).  
   - **Screenshot:**
<img src="assets/Screenshot 2025-03-14 184016.png" alt="">
   
3. **Data Transformation:**  
   - Adjust feature skewness.  
   - Transform quality scores into categories (if needed) for classification.
   
4. **Feature vs. Quality Analysis:**  
   - Visualize the relationship between individual features (like volatile acidity or citric acid) and wine quality.  
   - **Screenshots:**
   <img src="assets/Screenshot 2025-03-14 184036.png" alt="">
   <img src="assets/Screenshot 2025-03-14 184025.png" alt="">
   
5. **Model Training and Evaluation:**  
   - Split the data into training and testing sets.  
   - Train multiple models and evaluate their performance using metrics like accuracy and ROC curves.

---

## Data Analysis Insights

- **Distribution Adjustments:**  
  Many features had skewed distributions. Adjustments (e.g., logarithmic transformations) helped normalize these distributions.
  
- **Correlation Analysis:**  
  A correlation matrix revealed significant relationships between features and wine quality. For instance, variations in acidity and alcohol content were closely related to quality scores.
  
- **Feature Importance:**  
  Visualizations, such as barplots, showed how features like volatile acidity and citric acid impact wine quality. These insights guided our feature selection and model tuning.

---

## Recommendations for Wine Producers

Based on our analysis and model predictions, here are some actionable recommendations:

- **Acidity Balance:**  
  Monitor both total and volatile acidity carefully. Experiment with different levels during winemaking to achieve the desired flavor profile.
  
- **Alcohol Content:**  
  Adjust the alcohol content to suit the style of wine. Different wine types benefit from different alcohol levels.
  
- **Quality Evaluation:**  
  Use the predictive model as a quality control measure during production to estimate the wine's quality based on measurable properties.
  
- **Consistency:**  
  Standardize production processes to ensure consistent quality, which is vital for building a strong brand reputation.

---

## How to Run the Project

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/valusanikil/wine-quality-prediction.git
   cd wine-quality-prediction
   ```

## Technologies and Tools

- **Programming Language:** Python  
- **Libraries:**  
  - NumPy  
  - Pandas  
  - Matplotlib  
  - Seaborn  
  - Scikit-learn  
- **Environment:** Jupyter Notebook
