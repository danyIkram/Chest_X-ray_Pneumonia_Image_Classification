# 🩺 Chest X-ray Pneumonia Classification – Streamlit Web App

This repository contains a **Streamlit web application** that uses a pre-trained deep learning model to classify chest X-ray images into:
- **NORMAL**
- **PNEUMONIA**

The model was trained using a Convolutional Neural Network (CNN) in a **separate repository**:  
➡ [model_for_Chest_X-ray_Pneumonia_Image_Classification_project](https://github.com/danyIkram/model_for_Chest_X-ray_Pneumonia_Image_Classification_project)
---

> ⚠️ **Note:** The `.gitignore` excludes large files like `pneumonia_classifier.h5` and `.webm` video.  
> You need to manually place the trained model inside `models/` before running the app.

---

## Dataset

We used the publicly available **Chest X-ray Images (Pneumonia)** dataset from [Mendeley Data](https://data.mendeley.com/datasets/rscbjbr9sj/2):

- **NORMAL images:** 1,349  
- **PNEUMONIA images:** 3,884  
- **Observation:** The dataset is **imbalanced**, containing almost 3× more pneumonia cases.

---

[Watch Demo Video](https://drive.google.com/file/d/1MAKSVzQKty2Z_DfO3l_2NiAIlQOMGnJE/view?usp=sharing)


## Model Performance

### Confusion Matrix (Test Set)

|                | Predicted NORMAL | Predicted PNEUMONIA |
|----------------|----------------|---------------------|
| **Actual NORMAL**   | **155** ✅          | **79** ❌               |
| **Actual PNEUMONIA**| **21** ❌           | **369** ✅              |

### Interpretation
- **True Positives:** 369 pneumonia cases correctly classified  
- **True Negatives:** 155 normal cases correctly classified  
- **False Positives:** 79 normal cases incorrectly classified as pneumonia  
- **False Negatives:** 21 pneumonia cases missed  

✅ **Strength:** High recall (most pneumonia cases are detected)  
⚠️ **Limitation:** Some normal images are misclassified (false positives), which may lead to unnecessary re-checks, but this is often preferred over missing pneumonia cases.

---

