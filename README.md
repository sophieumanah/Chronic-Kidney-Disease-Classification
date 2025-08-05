# Chronic Kidney Disease (CKD) Classification

Hi, in this project, I explored the medical world of chronic kidney disease and built robust classification models to predict whether an individual has CKD based on clinical and demographic data.

The goal was clear: given a set of health-related attributes, how accurately can I predict CKD status? 

This project demonstrates a practical machine learning pipeline for handling healthcare classification problems.

The Jupyter Notebook walks through a complete end-to-end workflow from loading, cleaning, and exploring the data to building, evaluating, and comparing multiple models. Whether you're learning, hiring, or curious about healthcare data, you’ll find value in this notebook.

---

## 🎯 Objective  
To develop a classification model that accurately identifies individuals with chronic kidney disease using clinical and demographic features.

---

## 🧾 Dataset Overview  

Here’s what we’re working with:

| Feature                    | Description                                           |
|----------------------------|-------------------------------------------------------|
| age                        | Age of the individual                                |
| bp                         | Blood pressure                                       |
| sg                         | Urine specific gravity                               |
| al                         | Albumin levels                                       |
| su                         | Sugar levels                                         |
| rbc                        | Red blood cells                                      |
| pc                         | Pus cells                                            |
| pcc                        | Pus cell clumps                                      |
| ba                         | Bacteria presence                                    |
| bgr                        | Blood glucose random                                 |
| bu                         | Blood urea                                           |
| sc                         | Serum creatinine                                     |
| sod                        | Sodium levels                                        |
| pot                        | Potassium levels                                     |
| hemo                       | Hemoglobin                                           |
| pcv                        | Packed cell volume                                   |
| wc                         | White blood cell count                               |
| rc                         | Red blood cell count                                 |
| htn                        | Hypertension (yes/no)                                |
| dm                         | Diabetes mellitus (yes/no)                           |
| cad                        | Coronary artery disease (yes/no)                     |
| appet                      | Appetite status                                      |
| pe                         | Pedal edema (yes/no)                                 |
| ane                        | Anemia (yes/no)                                      |
| classification (target)   | CKD status (ckd / notckd)                            |

📌 **Problem Type**: Supervised Classification

---

## 🧰 Tools & Libraries Used  

This project was built with:

- Python 3  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  

---

## 🔍 Workflow & Approach  

### 1. Initial Data Checks  
- Loaded the dataset and reviewed its structure  
- Identified and handled missing values (Mseveral columns had missing data)  
- Cleaned and standardized categorical entries (e.g., inconsistent yes/no labels)  
- Converted numeric-like columns stored as strings to proper numerical types  

### 2. Exploratory Data Analysis (EDA)  
- Explored class distribution (minor imbalance but acceptable)  
- Visualized the relationship between CKD and key features using histograms  
- Noted that individuals with CKD often had abnormalities such as:  
  - Hypertension  
  - Diabetes mellitus  
  - Coronary artery disease  
  - Pedal edema  
  - Anemia  
  - Presence of pus cell clumps and bacteria  
- Observed strong correlations between `specific_gravity`, `hemoglobin`, and `packed_cell_volume`  

### 3. Preprocessing  
- Imputed missing numerical values using the mean  
- Filled categorical missing values with the mode  
- Encoded categorical variables using `LabelEncoder`  
- Created a list of numeric and categorical features to guide preprocessing  
- Split the dataset into training and testing sets (80/20 split)  

### 4. Modeling  
Trained and evaluated four classification models:
* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* K-Nearest Neighbors 

Evaluation metrics used:
- **Accuracy**  
- **Precision**  
- **Recall**  
- **F1-Score**  

---

## 🧠 Key Findings  


| Model               | Test Accuracy | Train Accuracy | Performance Summary                                                             |
|---------------------|---------------|----------------|---------------------------------------------------------------------------------|
| Logistic Regression | 96.25%        | 92.19%         | Solid balance between generalization and precision/recall                       |
| K-Nearest Neighbors | 93.75%        | 93.44%         | Slightly lower performance especially in class 0 recall                         |
| Decision Tree       | 98.75%        | 98.75%         | Extremely high accuracy — could hint at overfitting                             |
| Random Forest       | 98.75%        | 98.75%         | High performance like Decision Tree, but more robust due to ensemble learning   |


📌 **Random Forest Classifier** had the highest accuracy and offered a good trade-off between interpretability and performance. Feature importance analysis showed that `hemoglobin`, `specific_gravity`, and `serum_creatinine` were among the top predictors.

---

## 🧾 Conclusion  

The classification models built in this project were able to predict chronic kidney disease status with high accuracy. Random Forest stood out as the top performer, but Logistic Regression also provided valuable baseline insights.

The project showcases the practical steps involved in handling medical datasets, from preprocessing noisy data to interpreting model outputs responsibly. It also reinforces the need for domain knowledge when working in healthcare analytics.

---

## 💬 Got Feedback or Questions?  
I’d love to hear your thoughts.  
Feel free to open an issue or fork the repo and build on it.

## 📲 Want to reach out?

📬 Let’s connect on [LinkedIn](https://www.linkedin.com/in/enobong-umanah/)

🧠 Follow my learning process on [my blog](https://medium.com/@Sophieumanah)

