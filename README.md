# Deep-Learning Challenge  

## Alphabet Soup Foundation – Neural Network Model

This project develops a **deep learning neural network model** to help **Alphabet Soup Foundation** identify funding applicants most likely to use resources effectively. Using historical data, the model predicts whether a new applicant will successfully utilize allocated funds.

## 📂 **Dataset**
The dataset used for training is publicly available:  
🔗 **[charity_data.csv](https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv)**  

---

## 📁 **Files in This Repository**  

| **File**                                                     | **Description**                                      |
|-------------------------------------------------------------|------------------------------------------------------|
| `AlphabetSoupCharity_NNModel_Report.md`                     | Project summary report in Markdown format           |
| `Deep Learning Challenge/AlphabetSoupCharity.ipynb`         | Python script to build and train the base model     |
| `Deep Learning Challenge/AlphabetSoupCharity.h5`            | Saved Keras base model (HDF5 format)                |
| `Deep Learning Challenge/AlphabetSoupCharity_Optimized.ipynb` | Python script to build & train the optimized model  |
| `Deep Learning Challenge/AlphabetSoupCharity_Optimized.h5`  | Saved Keras optimized model (HDF5 format)           |
| `README.md`                                                | Project overview and usage instructions             |

---

## 📥 **Downloading Project Files Locally & Opening in Google Colab**

### **Step 1: Clone the Repository Locally**
Run the following command in your terminal:
```bash
git clone https://github.com/geraldine1456/deep-learning-challenge.git
cd YOUR-REPO
```
Then, open the Jupyter Notebook locally:
```bash
jupyter notebook YOUR-NOTEBOOK.ipynb
```

### **Step 2: Upload Files to Google Colab**
If you prefer running the notebook in **Google Colab**, follow these steps:
1. Open **Google Colab**: **[Google Colab](https://colab.research.google.com/)**
2. Click `Upload` in the **File Panel** (left sidebar).
3. Select the notebook (`.ipynb`)
4. Start running the code in Colab!

---
## 🧪 Model Architecture Summary

* **Input Features**: 9 (scaled + encoded)
* **Hidden Layers**:
  * Layer 1: 80 neurons, ReLU
  * Layer 2: 40 neurons, ReLU
  * Layer 3: 10 neurons, ReLU
* **Output Layer**: 1 neuron, Sigmoid (binary classification)
* **Epochs**: 80
* **Loss**: Binary Crossentropy
* **Optimizer**: Adam
* **Final Accuracy**: **79.73%**

---

## 🔁 Future Improvements

* Hyperparameter tuning with Keras Tuner
* Try tree-based models (Random Forest, XGBoost)
* Use SHAP or LIME for model interpretability


