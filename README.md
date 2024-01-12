# Cirrhosis Prediction
Ashik Sathiya
---

## Cirrhosis Prediction - Data Cleaning
### Overview
This Jupyter notebook is part of a project focused on predicting cirrhosis. The primary goal of this notebook is to clean and prepare the dataset for further analysis and model building. This notebook is intended for data scientists, researchers, and anyone interested in medical data analysis, specifically in the domain of cirrhosis prediction.

### Features
Data Cleaning: Detailed steps to clean the dataset, including handling missing values, outliers, and data transformation.
Data Exploration: Initial exploration of data to understand the features and their characteristics.
Data Visualization: Basic visualizations to understand the distribution and relationship between different variables.

## Business Problem
Cirrhosis is an advanced liver condition caused by various liver diseases, including hepatitis and chronic alcoholism. A Mayo Clinic trial focused on primary biliary cirrhosis (PBC) collected data from 424 patients referred to the clinic over ten years. Among them, 312 patients took part in a randomized drug trial, while the remaining 112 patients consented to basic measurements and survival monitoring. However, six of the latter group were lost to follow-up, leaving data on 106 non-participating cases and the 312 participants in the randomized trial. The goal is to predict the Stage of Cirrhosis the Patient is in.

### Attribute Information
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
## K-Nearest Neighbors (KNN)
The K-Nearest Neighbors (KNN) model initially revealed varying class-specific performances. Notably, class 4 demonstrated superior results, especially in precision, recall, and F1-score metrics.

Upon fine-tuning with GridSearchCV, the KNN model showed minor yet notable improvements. These enhancements were primarily observed in class 4's predictive accuracy. This suggests a refined sensitivity of the model towards this specific class.

Incorporating Principal Component Analysis (PCA) into the KNN model maintained the trend of class-specific performance. This consistency across various configurations highlights the robustness of the KNN model in handling multiclass predictions, particularly for class 4.

Overall, the KNN models displayed commendable consistency in accuracy and F1-scores. This aspect underscores their potential utility in classifying stages of cirrhosis with precision.

## Decision Tree
The Decision Tree models exhibited a pattern akin to KNN in terms of class-specific performance. Class 4, in particular, achieved the highest performance in the model's default configuration.

Post optimization, the Decision Tree model displayed slight improvements in certain metrics. However, this was accompanied by a reduction in overall accuracy and F1-scores, indicating a nuanced balance between general accuracy and class-specific precision.

The application of PCA in the third Decision Tree model variant did not significantly alter this performance pattern. This suggests a stable classification behavior of the Decision Tree model across different configurations.

## Logistic Regression
Logistic Regression models showed a similar trend, with class 4 consistently achieving the best performance. This was evident in both the default and the fine-tuned models.

The introduction of PCA in the Logistic Regression model resulted in stable, albeit slightly varied, performance across different metrics. This stability is indicative of the model's robustness in multiclass classification, particularly relevant in medical datasets such as cirrhosis staging.

# Recommendation
The closely matched performance of all evaluated models makes selecting a single best model challenging. The decision must extend beyond mere performance metrics to include aspects like interpretability and computational efficiency.

Exploring ensemble methods could leverage the strengths of individual models for improved overall performance. Additionally, addressing class imbalances, applying advanced algorithms, conducting comprehensive feature engineering, and extensive hyperparameter tuning are crucial.

The journey towards an optimal model for accurately predicting the stage of Cirrhosis involves iterative experimentation and refinement. A holistic approach, encompassing all these factors, is recommended for developing an effective and reliable predictive model.
