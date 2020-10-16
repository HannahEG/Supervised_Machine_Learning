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

All models utilized on the loans dataset produced a precision score of .01 and 1 for high risk and low risk loan status, respectively. These models are not likely to positively predict high risk loans. It is as though each model predicted almost every loan would be low risk. Indeed, low risk loans are the majority loan. Varied and combination sampling did not mitigate this issue. Perhaps there is a level of overfitting at play.

However, the balance accuracy scores do vary with Random Oversampling model producing the highest results, .64.

Alternatively, the model which produced the best recall results were the Random Sampling and SMOTEENN models, with the SMOTEEN model producing a slightly better recall score for high risk loans. They were .71/.57 and .72/.57, respectively. 

All models for high risk F1 scores were equal to .02 with the exception of undersampling producing an F1 score equal to .01. The best Low risk F1 score belongs to SMOTE oversampling, which makes sense considering the original dataset had significantly more low risk loans.

In conclusion, both combination sampling and random oversampling are recommended models to evaluate these high risk and low risk loans, with random oversampling providing slightly better results overall. Random oversampling provides the highest balanced accuracy score at .64. SMOTEEN provides the lowest of all models utilized at .55.