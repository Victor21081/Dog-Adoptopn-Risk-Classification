# Dog Adoption Return Risk Classification

This project explores the use of machine learning classification methods to identify factors associated with dogs being returned to shelters after adoption. Using a simulated dataset of 42,000 adoption records, the project compares multiple classification algorithms and evaluates their ability to identify dogs at higher risk of being returned within 365 days.

The project focuses on understanding how different classification methods perform on an imbalanced dataset and which characteristics provide the strongest predictive signals. Four different classifiers are evaluated: **K-Nearest Neighbors, Multi-Layer Perceptron, Decision Tree, and Nearest Centroid**.

## Project Goals

* Identify factors associated with dog adoption returns
* Compare the performance of different machine learning classifiers
* Evaluate models using metrics appropriate for an imbalanced dataset
* Examine which features contribute most strongly to predictions
* Determine which classification approach is most useful for identifying higher-risk adoptions

## Methods

The project uses **Python** and **Scikit-Learn** to implement and evaluate the classification models.

Key methods include:

* Feature scaling
* One-hot encoding
* Stratified train/test splitting
* Cross-validation
* ROC-AUC
* Precision and recall
* Feature importance analysis

Because only approximately 15% of adoptions in the dataset result in a return, accuracy alone is not an appropriate measure of model performance. The project therefore focuses primarily on ROC-AUC, precision, and recall when comparing classifiers.

## Models

### K-Nearest Neighbors

Classifies adoptions based on the characteristics of similar observations in the dataset.

### Multi-Layer Perceptron

Uses a neural network to identify nonlinear relationships between adoption characteristics and return risk.

### Decision Tree

Creates a series of decision rules based on the features that best separate returned and non-returned adoptions.

### Nearest Centroid

Classifies observations according to their distance from the average feature profile of each outcome class.

## Results

Among the four classifiers, the **Multi-Layer Perceptron achieved the highest ROC-AUC of 0.7626** on the held-out data.

The analysis consistently identified **aggression score** as one of the strongest predictors of adoption returns. Other important factors included separation anxiety, reactivity toward other dogs, training level, adopter expectations, and energy mismatch.

Although the Multi-Layer Perceptron achieved the highest ROC-AUC, other models showed useful characteristics. For example, K-Nearest Neighbors achieved a similar ROC-AUC while identifying more of the actual returns, while Nearest Centroid offered faster computation with only a small difference in ROC-AUC.

## Dataset

The dataset contains **42,000 simulated adoption records** and 32 columns, including variables describing dog characteristics, behavior, adopter characteristics, and dog-adopter compatibility.

The dataset was simulated using statistics from real shelter data because information tracking whether an adoption remains successful after the dog leaves a shelter is limited.

## Research Paper

The complete methodology, analysis, visualizations, and results are available in the research paper included in this repository.

**Authors:**
Victor Carrillo, 
Matthew Akins, 
Juna Choi.
