# Supervised Machine Learning
## Loan Status Modeling

Presented a table of loan information, the following provides a results of high vs low risk loans using the following models:

### Model 1a: Naive Random Oversampling

Utilizing RandomOverSampler from the imblearn library:
- The balanced accuracy score is .64.
- Precision score: 
  * High Risk - .01
  * Low Risk - 1
- Recall score:  
  *  High Risk - .71
  *  Low Risk - .57
-  F1 score:
   *  High Risk - .02
   *  Low Risk - .73

### Model 1b: SMOTE Oversampling
Utilizing SMOTE from imblearn library:
- The balanced accuracy score is .61.
- Precision Score:
  * High Risk - .01
  * Low Risk - 1
- Recall score:
  - High Risk - .56
  - Low Risk - .66
- F1 score:
  - High Risk - .02
  - Low Risk - .79

### Model 2: Undersampling
Utilizing ClusterCentroids resampler from imblearn libary:
- The balanced accuracy score is .61.
- Precision score:
  - High Risk - .01
  - Low Risk - 1
- Recall score:
  - High Risk - .69
  - Low Risk - .41
- F1 score:
  - High Risk - .01
  - Low Risk - .58


### Model 3: Combination Sampling
Utilizing SMOTEENN from imblearn library:
- The balanced accuracy score is .55.
- Precision Score: 
  - High Risk - .01
  - Low Risk - 1
- Recall score:
  - High Risk - .72
  - Low Risk - .57
- F1 score:
  - High Risk - .02
  - Low Risk - .73

## Analysis/Conclusions

