# Breast Cancer detection

* Read breast cancer data which includes features as mean radius, mean area, texture, etc. The features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image.
* The target is either M (malicious) or B (benign)
* Scaled the dataset with StandardScaler()
* Transformed the target M / B --> 0 / 1
* Plotted the distribution of the features
* Evaluated the correlation between the features and the target
* Selected features with recursive feature elimination with cross validation (rfecv)
* Selected model based on Accuracy and Recall Scores
* Evaluated the confusion matrix

## Results:
| Model | Accuracy | Recall | F1-Score | Precision | AUC |
| --- | --- | --- | --- | --- | --- |
| Logistic Regression | 0.979 | 0.962 | 0.971 | 0.981 | 0.976 |
| Gradient Boosting | 0.972 | 0.981 | 0.962 | 0.945 | 0.974 |
| Random Forest | 0.965 | 0.981 | 0.954 | 0.929 | 0.968 |
| SVC | 0.958 | 0.943 | 0.943 | 0.943 | 0.955 |

**Logistic Regression** and **Gradient Boosting** have the best Accuracy Score. Gradient Boosting has a higher Recall Score which might be critical in this case because this means that there will be less undetected malicious diagnosis. See the following confusion matrices. The Gradient Boosting Model has only one malicious diagnosis misclassified as benign whereas the Logistic Regression Model has two malicious diagnosis misclassified as benign.

## Confusion Matrix:
<img src="https://github.com/janS95/breast_cancer_detection/blob/main/images/confusion_matrix_logistic_regression.png">

<img src="https://github.com/janS95/breast_cancer_detection/blob/main/images/confusion_matrix_gradient_boosting.png">

