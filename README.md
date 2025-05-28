# Dry Bean Classification Project

## Overview
This project focuses on classifying dry beans into seven distinct categories (SIRA, SEKER, DERMASON, CALI, BARBUNYA, HOROZ, BOMBAY) using a neural network implemented in R. The dataset contains 16 numerical features and 13,611 samples. The goal is to build a model that accurately predicts the bean class based on its features.

## Dataset
- **Source**: `Lecture_10_Dry_Bean_Dataset.csv`
- **Features**: 16 numerical attributes describing physical properties of the beans.
- **Target Variable**: `Class` (7 categories).
- **Size**: 13,611 samples.

## Key Steps
1. **Data Exploration**:
   - Visualized numerical features using scatter plots and box plots.
   - Checked for missing values (none found).
   - Observed class imbalance and addressed it using class weights.

2. **Preprocessing**:
   - Shuffled the dataset to avoid bias.
   - Split the data into training (80%) and testing (20%) sets.
   - Scaled features using standardization.

3. **Model Building**:
   - Constructed a neural network with:
     - Input layer (16 neurons)
     - Two hidden layers (128 and 64 neurons) with ReLU activation.
     - Output layer (7 neurons for classification).
   - Used weighted cross-entropy loss to handle class imbalance.
   - Optimized with Adam (learning rate = 0.005).

4. **Training**:
   - Trained for 300 epochs.
   - Achieved ~93% accuracy on both training and test sets.

## Results
- **Confusion Matrix**: Generated for the test set.
- **Accuracy**: Approximately 93%.

## Files
- **R Markdown**: `tereshchenko_assignment4.Rmd` (contains full code and analysis).
- **Dataset**: `./data/Lecture_10_Dry_Bean_Dataset.csv`.

## Dependencies
- R libraries:
  - `data.table`
  - `plotly`
  - `torch`
  - `ROSE`

## How to Run
1. Ensure all dependencies are installed.
2. Place the dataset in the `./data` directory.
3. Run the R Markdown file (`tereshchenko_assignment4.Rmd`).

## Notes
- The project demonstrates effective handling of class imbalance and feature scaling.
- Further improvements could include hyperparameter tuning or experimenting with other architectures.
