# Cirrhosis Prediction
Ashik Sathiya
---

## Business Problem
Cirrhosis is an advanced liver condition caused by various liver diseases, including hepatitis and chronic alcoholism. A Mayo Clinic trial focused on primary biliary cirrhosis (PBC) collected data from 424 patients referred to the clinic over ten years. Among them, 312 patients took part in a randomized drug trial, while the remaining 112 patients consented to basic measurements and survival monitoring. However, six of the latter group were lost to follow-up, leaving data on 106 non-participating cases and the 312 participants in the randomized trial. Our goal is to predict the Stage of Cirrhosis the Patient is in.

Attribute Information
1) ID: unique identifier
2) N_Days: number of days between registration and the earlier of death, transplantation, or study analysis time in July 1986
3) Status: status of the patient C (censored), CL (censored due to liver tx), or D (death)
4) Drug: type of drug D-penicillamine or placebo
5) Age: age in [days]
6) Sex: M (male) or F (female)
7) Ascites: presence of ascites N (No) or Y (Yes)
8) Hepatomegaly: presence of hepatomegaly N (No) or Y (Yes)
9) Spiders: presence of spiders N (No) or Y (Yes)
10) Edema: presence of edema N (no edema and no diuretic therapy for edema), S (edema present without diuretics, or edema resolved by diuretics), or Y (edema despite diuretic therapy)
11) Bilirubin: serum bilirubin in [mg/dl]
12) Cholesterol: serum cholesterol in [mg/dl]
13) Albumin: albumin in [gm/dl]
14) Copper: urine copper in [ug/day]
15) Alk_Phos: alkaline phosphatase in [U/liter]
16) SGOT: SGOT in [U/ml]
17) Triglycerides: triglicerides in [mg/dl]
18) Platelets: platelets per cubic [ml/1000]
19) Prothrombin: prothrombin time in seconds [s]
20) Stage: histologic stage of disease (1, 2, 3, or 4)


## Insights

<img width="710" alt="Screen Shot 2023-08-09 at 1 23 53 PM" src="https://github.com/AshikSathiya/Cirrhosis-Prediction/assets/92455762/72e11dec-d91a-4152-b4ab-82bd171f6ea2">


<img width="596" alt="Screen Shot 2023-08-09 at 1 24 10 PM" src="https://github.com/AshikSathiya/Cirrhosis-Prediction/assets/92455762/2cf8f625-db1f-445c-913b-42348b68f351">

# Results from Models

For KNN, the default model presents varying class-specific metrics, with class 4 demonstrating the highest performance. Subsequent fine-tuning through GridSearchCV leads to minor enhancements in precision, recall, and F1-score, with class 4 still displaying improved results. Principal Component Analysis (PCA) maintains this pattern of performance in the third model. Overall accuracy and F1-scores are consistent across all KNN models.

Similarly, the Decision Tree models depict class-specific results, with class 4 achieving the highest performance in both the default and tuned configurations. The second model, post optimization, shows slight improvements in specific metrics, though the accuracy and F1-scores experience a reduction. The third model, employing PCA, maintains a comparable pattern of results.

In Logistic Regression, class 4 again achieves the best performance in both the default and tuned models. However, the PCA-adjusted model exhibits consistent performance with slight variations in metrics.


# Recomendation
Considering the close performance of all models, a single recommended model is challenging to uncertain. Factors such as interpretability and computational efficiency may guide the choice. Additionally, exploring ensemble methods, addressing class imbalances, advanced algorithms, feature engineering, and hyperparameter tuning could contribute to further performance enhancement. The process of experimentation and refinement is crucial to achieve the best model for the predicting the Stage of Cirrhosis accurately.
