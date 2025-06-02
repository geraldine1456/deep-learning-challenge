
# 🧠 Neural Network Model Report for Alphabet Soup Foundation

## 1 . Overview of the Analysis

This analysis aimed to help the nonprofit foundation,  **Alphabet Soup**,  identify which funding applicants are most likely to be successful. By analyzing historical data on more than 34,000 past applicants, a binary classification deep learning model was created to predict whether a new applicant will effectively use the funds.

---

## 2. Results

### Data Preprocessing

- **Target Variable:**  
  - `IS_SUCCESSFUL` (1 = successful, 0 = not successful)

- **Feature Variables:**  
  - `NAME`, `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, `ASK_AMT`

- **Removed Variables:**  
  - `EIN` (identifier, not predictive)  
  - `STATUS` (provided no useful signal)  

---

###  Model Compilation, Training & Evaluation

#### **Model Architecture**
- **Layers:** 3 hidden layers + 1 output layer  
  - Using multiple hidden layers improves pattern recognition and non-linear relationships.
- **Neurons:**  
  - **Hidden Layer 1:** 80 neurons (captures a variety of features)  
  - **Hidden Layer 2:** 40 neurons (helps compress and abstract information)  
  - **Hidden Layer 3:** 10 neurons (fine-tunes higher-level representations)  
- **Activation Functions:**  
  - ReLU for hidden layers (fast learning, avoids vanishing gradient problem)  
  - Sigmoid for output layer (outputs probability between 0 and 1 for binary classification)  

#### **Model Perfomance**
- **Accuracy:** **79.73%** ✅ *(Target: 75%)*  
- **Loss:** **0.4629**  

---

### Steps Taken to Improve Performance
✔ Added a **third hidden layer** to enhance pattern recognition  
✔ Tuned **neuron counts** and **activation functions** for optimal learning  
✔ Reduced the number of **epochs** to mitigate overfitting  
✔ Dropped the `STATUS` column to remove noise  
✔ Included the `NAME` column to capture potential predictive signal  

---

## 3. Summary 

The neural network model achieved **79.73% accuracy**, surpassing the **75% target**.  While refining the model architecture yielded small gains, the **most significant improvement** came from including the `NAME` column. This suggests that organizational identity may carry meaningful historical or contextual signals predictive of success, though further analysis is needed to ensure it does not introduce bias.  The loss of **0.4629** indicates room for optimization  through regularization and hyperparameter tuning.


Although the neural network performed well, alternative models could provide better interpretability:**Tree-based Ensemble Methods** (e.g., Random Forest, XGBoost, LightGBM) may be more effective for **structured categorical data**.  These models often require **less preprocessing** and offer **greater transparency**—a key advantage for nonprofit stakeholders needing explainable funding decisions.

