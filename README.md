
# 🐧 Puffins Classifier

## Overview

This project develops a machine learning classifier to predict puffin species (`Arctica`, `Cirrhata`, `Corniculata`) based on body measurements such as body mass, wing length, beak length, and beak depth. Two models were explored: **Multinomial Logistic Regression** and **K-Nearest Neighbors (KNN)**, with further optimization using **GridSearchCV**.

---

## Dataset

The dataset consists of the following features:

- `body_mass_kg`: Body mass in kilograms
- `wing_length_m`: Wing length in meters
- `beak_length_mm`: Beak length in millimeters
- `beak_depth_mm`: Beak depth in millimeters
- `species`: The response variable (puffin species)

The dataset is loaded and cleaned by removing missing values (`NA`s) and ensuring that species names are consistent.

---

## Project Steps

### 1. Data Cleaning

- Missing values were dropped using the `dropna()` function.
- Species names were checked for consistency.
- Descriptive statistics were generated to ensure all feature values were coherent.

### 2. Data Visualization

- **Boxplots** were created to compare species differences in body mass, wing length, beak length, and beak depth.
- **Mean feature plots** were generated to visualize patterns across species and better understand species separation.

### 3. Model Building

Two different machine learning models were used to classify the puffin species:

- **Model 1: Multinomial Logistic Regression**
    - A multinomial logistic regression model was used to classify puffin species based on the four body measurement features.
    - The dataset was split into training and testing sets, and the model was evaluated using accuracy scores.

- **Model 2: K-Nearest Neighbors (KNN)**
    - KNN was initially trained with `k=3` neighbors, and the model was evaluated on the same test set.
    - Model accuracy was computed.

### 4. Model Optimization

- **GridSearchCV** was used to optimize the KNN model by identifying the best value of `k` based on cross-validation scores.
- The best-performing KNN model was evaluated (Model 3) using the optimal `k` value.

### 5. Results Visualization

- **Confusion matrices** were created to visualize the accuracy of both Model 1 (Logistic Regression) and Model 3 (Optimized KNN).
- Heatmaps were used to illustrate the confusion matrices, making it easier to interpret the model's predictions.

### 6. Performance Evaluation

- **Precision**, **recall**, and **F1-scores** were calculated for each model to compare their performance.
- **Model 1** (Logistic Regression) exhibited higher precision, recall, and F1-score than Model 3 (Optimized KNN), particularly for the `Corniculata` and `Cirrhata` species.
- However, both models had some difficulty correctly classifying the `Arctica` species.

---

## Conclusion

- **Model 1 (Multinomial Logistic Regression)** was chosen as the final model due to its superior performance in terms of precision, recall, and F1-score.
- Further improvements could be explored, including trying other classification techniques or addressing potential class imbalances.

---

## How to Run the Code

1. Install the necessary libraries:

    ```bash
    pip install pandas seaborn scikit-learn matplotlib
    ```

2. Clone this repository:

    ```bash
    git clone https://github.com/nicoleamorveli/puffins_classifier.git
    ```

3. Run the Jupyter notebook or Python script provided in the repository to train and test the models on the puffins dataset.

---

## Future Work

- Research other classification models such as **Random Forests** or **Support Vector Machines (SVM)**.
- Analyze the class distribution and potentially apply techniques like **oversampling** or **undersampling** to address any imbalances.
