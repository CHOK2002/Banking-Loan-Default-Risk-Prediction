# Banking-Loan-Default-Risk-Prediction

## Background
This project examines loan default prediction models to overcome the limitations of conventional banking systems by improving credit risk management through accurate predictions. While some models in this project have failed to significantly enhance the credit evaluation process, some have surprisingly demonstrated the ability to better assess borrowers' repayment capacities and support more informed lending decisions. The banking loan datasets used in this project are sourced from **Analytics Vidhya's Machine Learning Summer Training Hackathon**, where participants aim to achieve the highest possible accuracy using the provided training dataset.

## Methodology / Folders Breakdown
![image](https://github.com/user-attachments/assets/1ddb5bb5-f688-44ac-ab1c-1ac1141ef9a5)

## Result & Discussion

### ML Models
![image](https://github.com/user-attachments/assets/e1949d41-1cea-4fba-b277-ad501ce0c90d)

### Tree Based Models
![image](https://github.com/user-attachments/assets/bd67467c-ecdf-4e18-b61a-69ec14ea6014)

## Conclusion
After experimenting with various model architectures, including adjusting train-test split ratios, testing different feature combinations, and creating new features, the highest accuracy achieved across all models was only around 55-60%. This is because most models struggled to classify loan default samples effectively. Machine learning models, in particular, had precision, recall, and F1 scores for loan defaults below 40%. Similarly, tree-based models also performed poorly with recall and precision for loan defaults often under 40%.

Among all models, only one model which is Decision Tree (DT) showed balanced performance across precision, recall, and F1 scores, consistently exceeding 40%. However, it suffered from significant overfitting, with a training accuracy of nearly 100% compared to a validation accuracy of 53.70%. On the other hand, the KNN model, though it had a slightly lower loan default recall at 36%, demonstrated better generalization with a training accuracy of 70.82% and validation accuracy of **56.21%**. Additionally, the macro average and weighted average metrics for KNN were higher than those for the DT model, further supporting its robustness. Considering its stability, reduced overfitting, and superior overall metrics, **KNN** emerged as the **most suitable model** for this project.

There are two major problems that limit the model’s accuracy to 55-60% and prevent it from exceeding 70%. The first issue is the small dataset size with the training set containing only about 7,000 samples. This makes it challenging for the models to learn complex patterns effectively and achieve higher accuracy. Next, the second issue is the imbalance in the dataset. Loan default samples account for just over 2800, while non-default samples make up more than 4200. This imbalance causes the models to be biased toward the non-default class, further impacting the performance on loan default predictions. Hence, future improvements can primarily focus on addressing these two problems to enhance the model's accuracy and reliability.

## Benchmarking with Previous Hackthon Participants
Reference to https://www.analyticsvidhya.com/datahack/leaderboard/machine-learning-summer-training-hackathon
![image](https://github.com/user-attachments/assets/29056e31-2671-405c-a662-93135628b56d)

## Future Improvement
- **Handle data imbalance by using the techniques of SMOTE or ADASYN**
  - Use SMOTE or ADASYN techniques to oversampling the minority samples
  - Compare the training result which is better
- **Quality of Dataset**
  - Collect more data to increase the dataset size as 7000 data is too less to enable the models learn effectively
- **Different Models**
  - Train with deep learning models like ANN, RNN and ensemble learning models like voting and stacking classifier. 

    











