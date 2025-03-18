# **Neural Network Model for Alphabet Soup Report**

## **1. Overview of the Analysis**

The purpose of this project is to assist the non-profit organization *Alphabet Soup* in identifying the ideal candidates for funding by evaluating their chances of success in their projects. To achieve this, a binary classification model was developed to predict whether an organization will succeed using historical data.

Two versions of the model were created: an initial one and an optimized version, to compare their performance and fine-tune the parameters to achieve the highest possible accuracy.

---

## **2. Results**

### **a) Data Preprocessing**

**Key Questions and Answers:**

- **What is the target variable for the model?**  
  The target variable is `IS_SUCCESSFUL`, which indicates whether an organization effectively used the funding (1: successful, 0: not successful).

- **What are the feature variables for the model?**  
  The feature variables include all columns except `IS_SUCCESSFUL`, such as:  
  - `APPLICATION_TYPE` (Application type)  
  - `AFFILIATION` (Affiliated sector)  
  - `CLASSIFICATION` (Government classification)  
  - `USE_CASE` (Use case for funding)  
  - `INCOME_AMT` (Income classification)  
  - `ASK_AMT` (Funding amount requested), among others.

- **Which variables were removed and why?**  
  The columns `EIN` and `NAME` were removed because they do not provide direct predictive value for the model (they act as identifiers).

- **What additional adjustments were made in the optimized version?**  
  - In the optimized model, rare values in the `NAME` column (less than 5 occurrences) were grouped under the value "Other."

- **What techniques were used to process the data?**  
  - Rare values were grouped in the `APPLICATION_TYPE`, `CLASSIFICATION`, and `NAME` columns.  
  - Categorical columns were converted into numerical values using `pd.get_dummies()`.  
  - Data was scaled using `StandardScaler` to standardize the features.

---

### **b) Model Compilation, Training, and Evaluation**

**Key Questions and Answers:**

#### Initial Model

- **How many neurons, layers, and activation functions were used for the initial model?**  
  - **Hidden layers:** 2 hidden layers with ReLU activation:  
    - First layer: 5 neurons.  
    - Second layer: 3 neurons.  
  - **Output layer:** 1 neuron with Sigmoid activation (suitable for binary classification).

- **Performance of the initial model:**  
  - **Accuracy:** 72.86%  
  - **Loss:** 0.5579  
  Although functional, this model did not meet the target accuracy of 75%, highlighting the need for optimization.

#### Optimized Model

- **What changes were made in the optimized model?**  
  - **Hidden layers:** Dynamically adjusted the number of layers (up to 3 layers).  
  - **Neurons per layer:** The number of neurons was dynamically determined, with a maximum of 13.  
  - **Data:** Additional adjustments to categorical values were made to reduce noise.

- **Performance of the optimized model:**  
  - **Accuracy:** 79.29%  
  - **Loss:** 0.4538  
  This model surpassed the target accuracy of 75%, demonstrating that the adjustments significantly improved its performance.

---

## **3. General Summary**

- **Results:**  
  - The initial model achieved a moderate accuracy of 72.86% but did not meet the target.  
  - The optimized model, with adjustments to the layers and neurons, improved its performance, achieving an accuracy of 79.29%.

- **Recommendation:**  
  While the neural network model was effective after optimization, it might be worth exploring other algorithms such as **Random Forest** or **XGBoost**, which handle categorical data well and are less sensitive to specific configurations.

---