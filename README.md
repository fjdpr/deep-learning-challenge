# Deep Learning Challenge: Alphabet Soup Neural Network

## Summary
This project focuses on building a binary classification model to assist the non-profit organization **Alphabet Soup** in identifying the best candidates for funding. The model predicts the success likelihood of applicants based on historical data.

Two versions of the model were created:
1. **Initial Model**: A basic implementation of a neural network.
2. **Optimized Model**: A refined version with adjustments for improved performance.

---

## Objectives
- Develop a deep learning model using TensorFlow and Keras.
- Preprocess categorical and numerical data for machine learning.
- Build, train, and evaluate an initial neural network model.
- Optimize the model to achieve a target accuracy of **75%** or higher.
- Compare the performance of the initial and optimized models.

---

## Data Description
The dataset includes information about organizations funded by **Alphabet Soup**:
- **EIN and NAME**
- **APPLICATION_TYPE**
- **AFFILIATION**
- **CLASSIFICATION**
- **USE_CASE**
- **ORGANIZATION**
- **STATUS**
- **INCOME_AMT**
- **SPECIAL_CONSIDERATIONS**
- **ASK_AMT**
- **IS_SUCCESSFUL**

---

## Included Scripts
1. **AlphabetSoupCharity.ipynb**:
   - Loads and preprocesses the dataset.
   - Encodes categorical variables and scales numerical features.
   - Builds, trains, and evaluates the initial neural network model.
   - Exports the trained model as `AlphabetSoupCharity.h5`.

2. **AlphabetSoupCharity_Optimization.ipynb**:
   - Repeats data preprocessing.
   - Implements multiple optimization techniques to improve model performance:
     - Adjusts the number of layers and neurons dynamically.
     - Modifies hyperparameters (e.g., activation functions).
     - Refines the treatment of rare categorical values.
   - Trains and evaluates the optimized neural network.
   - Exports the optimized model as `AlphabetSoupCharity_Optimization.h5`.

---

## Requirements

### Installing Required Libraries
Ensure you have Python installed on your machine. Then, install the required libraries using pip:
```bash
pip install pandas numpy scikit-learn tensorflow
```

### Instructions

## Open the Notebooks in Google Colab
Click the buttons below to directly open the notebooks in Google Colab:

- **AlphabetSoupCharity.ipynb**  
  <a href="https://colab.research.google.com/github/fjdpr/deep-learning-challenge/blob/main/AlphabetSoupCharity/AlphabetSoupCharity.ipynb" target="_parent"> 
      <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/> 
  </a>

- **AlphabetSoupCharity_Optimization.ipynb**  
  <a href="https://colab.research.google.com/github/fjdpr/deep-learning-challenge/blob/main/AlphabetSoupCharity/AlphabetSoupCharity_Optimization.ipynb" target="_parent"> 
      <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/> 
  </a>

---

## Features

### Data Preprocessing
- Encodes categorical variables with `pd.get_dummies`.
- Scales numerical data using `StandardScaler`.
- Handles rare categorical values by grouping them into an "Other" category.

### Initial Neural Network
- Two hidden layers with ReLU activation functions.
- Output layer with Sigmoid activation for binary classification.

### Optimization Techniques
- Increased the number of layers and neurons dynamically.
- Fine-tuned hyperparameters (e.g., activations, epochs).
- Improved data preprocessing (handling rare values and scaling).

---

## Contributions
We welcome and appreciate contributions from the community. If you have suggestions or improvements, please open an issue or submit a pull request.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.
