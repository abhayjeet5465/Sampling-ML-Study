# Sampling-ML-Study
By: Abhayjeet(102303761)
## Abstract
Imbalanced datasets pose a significant challenge in machine learning as they often bias models toward the majority class. This study investigates the impact of different sampling and validation techniques on the performance of multiple machine learning models using a highly imbalanced credit card dataset. Five techniques—Simple Random Sampling, Stratified Sampling, Cluster Sampling, Bootstrap Sampling, and Cross-Validation—are applied and evaluated across five classifiers. The results highlight how sampling strategy selection directly influences model accuracy.

---

## I. Introduction
In real-world applications, datasets are frequently imbalanced, leading to poor predictive performance and misleading accuracy metrics. Sampling techniques are commonly used to address this issue by restructuring the dataset before model training. This project analyzes how different sampling approaches affect model accuracy and stability when applied to an imbalanced credit card fraud dataset.

---

## II. Dataset Description
The dataset used in this study is a credit card transaction dataset containing a severe class imbalance between fraudulent and non-fraudulent transactions.

- Source: Creditcard_data.csv
- Target Variable: `Class`
- Class 0: Non-Fraud
- Class 1: Fraud

---

## III. Sampling and Validation Techniques

### A. Simple Random Sampling
Simple Random Sampling selects data points randomly from the population, ensuring that each instance has an equal probability of selection. This technique preserves the overall distribution of the dataset and performed best across most models.

### B. Stratified Sampling
Stratified Sampling divides the dataset into strata based on class labels and samples proportionally from each class. This ensures that class imbalance is maintained in both training and testing datasets.
                                        
### C. Cluster Sampling
In Cluster Sampling, the dataset is divided into multiple clusters based on index grouping. A subset of clusters is randomly selected, and all data points within those clusters are used for training. This method may lose global data patterns if clusters are not representative.

### D. Bootstrap Sampling
Bootstrap Sampling generates new datasets by sampling with replacement from the original dataset. This technique reduces variance and is particularly effective for models sensitive to data distribution changes.

### E. Cross-Validation
Stratified K-Fold Cross-Validation is used to evaluate model performance without altering the dataset. It provides reliable and unbiased performance estimates by training and testing the model across multiple folds.

---

## IV. Machine Learning Models Used

- M1: Logistic Regression  
- M2: Decision Tree Classifier  
- M3: Random Forest Classifier  
- M4: Support Vector Machine  
- M5: K-Nearest Neighbors  

---

## V. Experimental Results

### Table I: Accuracy (%) of Models Using Different Techniques

| Model | Simple Random | Stratified | Cluster | Bootstrap | Cross Validation |
|------|---------------|------------|---------|-----------|------------------|
| M1 | 99.38 | 98.71 | 97.84 | 97.41 | 98.70 |
| M2 | 98.77 | 98.71 | 94.96 | 99.14 | 98.19 |
| M3 | 99.38 | 98.71 | 97.84 | 98.71 | 98.83 |
| M4 | 99.38 | 98.71 | 97.84 | 97.41 | 98.83 |
| M5 | 99.38 | 98.71 | 97.84 | 97.41 | 98.83 |

---

## VI. Best Sampling Technique per Model

| Model | Best Technique | Accuracy (%) |
|------|---------------|--------------|
| M1 | Simple Random Sampling | 99.38 |
| M2 | Bootstrap Sampling | 99.14 |
| M3 | Simple Random Sampling | 99.38 |
| M4 | Simple Random Sampling | 99.38 |
| M5 | Simple Random Sampling | 99.38 |

---

## VII. Discussion
The results demonstrate that Simple Random Sampling achieves the highest accuracy for the majority of models, indicating its effectiveness in maintaining the original data characteristics. Bootstrap Sampling performs best for one model due to its variance-reducing property. Stratified Sampling provides consistent but slightly lower accuracy. Cluster Sampling shows the weakest performance, as partial cluster selection may omit important patterns. Cross-Validation offers stable and reliable evaluation but is not a balancing technique.

---

## VIII. Conclusion
This study confirms that the choice of sampling technique significantly affects machine learning model performance on imbalanced datasets. Simple Random Sampling emerged as the most effective technique overall, while Bootstrap Sampling proved beneficial for specific models. The findings emphasize that no single sampling method is universally optimal and must be selected based on the model and dataset characteristics.

---


---

## Author
Abhayjeet  
B.Tech Computer Engineering  
Thapar Institute of Engineering and Technology
