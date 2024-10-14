# Puffins Classifier

## Overview
This project develops a machine learning classifier to predict puffin species (*Arctica*, *Cirrhata*, *Corniculata*) based on body measurements like body mass, wing length, beak length, and beak depth. Two models were explored: **Multinomial Logistic Regression** and **K-Nearest Neighbors (KNN)**, with further optimization using grid search.

## Dataset
The dataset consists of the following features:
- **Body mass (kg)**
- **Wing length (m)**
- **Beak length (mm)**
- **Beak depth (mm)**
- **Species** (response variable)

## Project Steps

### 1. Data Cleaning
- Missing values were dropped with `dropna()`.
- Species names were checked for consistency.
- Descriptive statistics were used to ensure the features had coherent values.

### 2. Data Visualization
- **Boxplots** were created to compare species differences in body mass, wing length, beak length, and beak depth.
- **Mean feature plots** were generated to visualize patterns across species.

### 3. Model Building

#### Model 1: Multinomial Logistic Regression
- Multinomial logistic regression was used to classify the puffin species.
- Data was split into training and testing sets, and the model was evaluated using an accuracy score.

#### Model 2: K-Nearest Neighbors (KNN)
- KNN was employed with an initial value of 3 neighbors.
- Similar training and testing splits were used, and the model’s accuracy was measured.

### 4. Model Optimization
- **GridSearchCV** was used to identify the optimal number of neighbors (K) for KNN.
- The best-performing model (Model 3) was evaluated using the optimal K value.

### 5. Results Visualization
- **Confusion matrices** were generated for Model 1 and Model 3 to visualize prediction accuracy.
- **Heatmaps** were used to show these confusion matrices.

### 6. Performance Evaluation
- Precision, recall, and F1-scores were computed for each model.
- **Model 1 (Logistic Regression)** outperformed **Model 3 (Optimized KNN)**, particularly for the *Corniculata* and *Cirrhata* species, though both models struggled with classifying the *Arctic* species.

## Conclusion
Model 1 (Logistic Regression) was selected as the final model due to higher precision, recall, and F1-scores. Further exploration could involve testing other classification techniques or addressing class imbalance.

## How to Run the Code
1. Install the necessary libraries:
   ```bash
   pip install pandas seaborn scikit-learn matplotlib



