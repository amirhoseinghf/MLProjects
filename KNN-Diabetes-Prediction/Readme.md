# KNN Diabetes Prediction - Documentation

## Overview
This project implements a K-Nearest Neighbors (KNN) classifier to predict whether a person has diabetes based on diagnostic measurements. The model is trained on the Pima Indians Diabetes Dataset, which contains medical data from 768 patients.

## Dataset
The dataset consists of the following features:
- Pregnancies: Number of times pregnant
- Glucose: Plasma glucose concentration
- BloodPressure: Diastolic blood pressure (mm Hg)
- SkinThickness: Triceps skin fold thickness (mm)
- Insulin: 2-Hour serum insulin (mu U/ml)
- BMI: Body mass index (weight in kg/(height in m)^2)
- DiabetesPedigreeFunction: Diabetes pedigree function
- Age: Age in years
- Outcome: Class variable (0 or 1)

Dataset size: 768 records

## Data Preprocessing
1. **Handling Missing Values**: 
   - Zero values in Glucose, BloodPressure, SkinThickness, Insulin, and BMI columns were replaced with NaN
   - NaN values were then filled with the mean of their respective columns

2. **Train-Test Split**:
   - Data was split into 80% training and 20% testing sets
   - Random state was fixed for reproducibility

3. **Feature Scaling**:
   - StandardScaler was used to normalize the features (mean=0, variance=1)
   - Important for KNN as it's distance-based

## Model Training
- **Algorithm**: K-Nearest Neighbors Classifier
- **Parameters**:
  - n_neighbors = 11
  - metric = 'euclidean'
  - p = 2 (equivalent to Euclidean distance)

## Evaluation Metrics
The model was evaluated using:
1. **Confusion Matrix**:
   ```
   [[94 13]
    [15 32]]
   ```
   - True Negatives: 94
   - False Positives: 13
   - False Negatives: 15
   - True Positives: 32

2. **F1 Score**: 0.6957

3. **Accuracy**: Can be calculated from the confusion matrix as (TP+TN)/(TP+TN+FP+FN)

## How to Use
1. Clone the repository
2. Ensure you have Python 3.x and required libraries installed (pandas, numpy, scikit-learn)
3. Run the Jupyter notebook `KNN_Diabetes_Prediction.ipynb`
4. The notebook will:
   - Mount Google Drive (if using Colab)
   - Load and preprocess the data
   - Train the KNN model
   - Evaluate performance

## Dependencies
- Python 3.x
- pandas
- numpy
- scikit-learn
- Jupyter Notebook (for running the .ipynb file)

## Future Improvements
1. Experiment with different values of k (number of neighbors)
2. Try different distance metrics (Manhattan, Minkowski)
3. Implement cross-validation for more robust evaluation
4. Address class imbalance if present
5. Feature selection to identify most important predictors

## Author
[Your Name]

## License
[MIT License] or specify your preferred license