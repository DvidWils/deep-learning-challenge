# Module 21: Neural Networks and Deep Learning Challenge - Alphabet Soup
## Overview

The goal of this challenge was to help the nonprofit Alphabet Soup improve its funding decision process. Through training with historical data on previous applicants, a binary classification model was built using TensorFlow and Kerasto to predict whether applicants would be successful after receiving funding.

---

## Data Preprocessing

- **Target Variable:** `IS_SUCCESSFUL` – Indicates whether the funded organization was successful.
- **Features:** All columns except `EIN` and `NAME`, which were removed due to being identifiers.
- low frequency categorical values in `APPLICATION_TYPE` and `CLASSIFICATION` were consolidated into `"Other"`.
- Categorical variables were encoded using one-hot encoding.
- Feature scaling was performed using `StandardScaler()` ofr performance improvement.

---

## Baseline Model – `Starter_Code.ipynb`

- **Architecture:**
  - Two hidden layers: 80 and 30 neurons (ReLU)
  - Output layer: 1 unit (Sigmoid)
- Epochs: 150

  ![image](https://github.com/user-attachments/assets/ff45b656-1b2e-4130-9e9f-e85655cf693d)
  ![image](https://github.com/user-attachments/assets/fec605a7-bb2e-42b7-9508-f594cc280062)

- **Performance:** Accuracy reached approximately 72.42%

---

## Optimized Model – `AlphabetSoupCharity_Optimization.ipynb`

- **Architecture:**
  - Three hidden layers: 256, 128, and 64 neurons (ReLU)
  - Output layer: 1 unit (Sigmoid)
- Epochs: 200

- **Optimizations Applied:**
  - Increased number of layers (depth) and neurons (complexity)
  - Trained for more epochs
  - Adjusted threshold for grouping rare values in categorical columns

  ![image](https://github.com/user-attachments/assets/ac82bed0-a6ce-4716-89f1-a90c48d14112)
  ![image](https://github.com/user-attachments/assets/68098ec2-77fb-4c3b-a1a7-db2defc6e86e)

- **Performance:** Accuracy improved slightly to around 72.86%

---

## Conclusion

 The optimized model showed a small improvement in performance, however, it did not surpass the 75% target threshold.  The results suggest that deep learning performs reasonably well butother models may be worth exploring. Tree-based models like Random Forest could be tested in the future, as they often perform well with structured/tabular data similar to the data used in this challenge.
