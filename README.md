# Cardiovascular Risk Prediction

## About the Project
This project implements a Logistic Regression model to predict Coronary Heart Disease (CHD) risk based on the Framingham Heart Study dataset. The main objective is to create a predictive model that can help identify individuals at risk for CHD.

### Key Features:
- Logistic Regression model tuned for optimal performance using GridSearchCV.
- Addressed class imbalance using Synthetic Minority Oversampling Technique (SMOTE).
- Evaluated using metrics like Accuracy, Precision, Recall, F1-score, and ROC-AUC.
- Visualized key metrics to assess model performance.
- Saved the best model for future use.

---

## Dataset
The project utilizes the **Framingham Heart Study Dataset**, which is widely used for cardiovascular risk analysis. This dataset contains medical and demographic information related to cardiovascular health.

### Key Features:
- **Total Rows**: 61,771
- **Total Columns**: 15
- **Important Variables**:
  - Age
  - Gender
  - Blood Pressure
  - Cholesterol Levels
  - Smoking Status
  - Diabetes

### Preprocessing Steps:
- Handled missing values by imputing or removing incomplete rows.
- Applied feature scaling for numerical attributes.
- Addressed class imbalance using **SMOTE**.

---

## Results
The performance of the Logistic Regression model on the test dataset is summarized below:

### **Best Model Accuracy**
- **Accuracy**: 91.90%

### **Classification Report**
| Metric         | Class 0 (No CHD) | Class 1 (CHD) | Macro Avg | Weighted Avg |
|----------------|------------------|---------------|-----------|--------------|
| **Precision**  | 0.92             | 0.49          | 0.70      | 0.89         |
| **Recall**     | 1.00             | 0.02          | 0.51      | 0.92         |
| **F1-Score**   | 0.96             | 0.03          | 0.50      | 0.88         |
| **Support**    | 56,774           | 4,997         | -         | 61,771       |

### **Key Observations**
- The model achieved high accuracy of **91.90%**, driven by its strong performance on the majority class (Class 0 - No CHD).
- The model struggled to predict the minority class (Class 1 - CHD), with low precision and recall values.
- **Class Imbalance**: This result highlights the challenge of imbalanced datasets, as the model performed better on the majority class due to its larger representation in the data.

### Visualizations
The following visualizations highlight the performance of the Logistic Regression model:

#### **1. Receiver Operating Characteristic (ROC) Curve**
This curve illustrates the trade-off between sensitivity (true positive rate) and specificity (1 - false positive rate).


#### **2. Precision-Recall Curve**
This curve emphasizes the balance between precision and recall, especially important for imbalanced datasets.



#### **4. Model Performance Metrics**
Bar chart comparing Accuracy, Precision, Recall, and F1-Score to evaluate the overall performance of the model.



#### **3. Confusion Matrix**
The confusion matrix visualizes the actual versus predicted classifications of the model.



![Model Performance Visualization](Results)

---

## Installation
To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Cardiovascular_Risk_Prediction.git
   ```

2. Navigate to the project directory:
   ```bash
   cd Cardiovascular_Risk_Prediction
   ```

3. Ensure you have the required Python libraries installed. The key dependencies are:
   - pandas
   - numpy
   - scikit-learn
   - matplotlib

   You can install these libraries using pip:
   ```bash
   pip install pandas numpy scikit-learn matplotlib
   ```

4. Run the Jupyter notebook or Python script to train the model and view the results.

---

## Future Improvements
- Experiment with ensemble models such as Random Forest or XGBoost to improve minority class predictions.
- Perform additional hyperparameter tuning to optimize performance further.
- Explore alternative techniques to address class imbalance, such as class weighting.
- Deploy the model using a web framework like Flask or Django for real-world usage.

---

## Acknowledgments
This project is based on the Framingham Heart Study dataset. For more information about the dataset and study, visit the [Framingham Heart Study Website](https://www.framinghamheartstudy.org/).

---

## Presentation
You can access the project presentation [here](presentation.pptx).

---

