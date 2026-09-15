# 🩺 Fetal Health Classification System

An AI-based healthcare project for fetal health assessment using **Cardiotocography (CTG) data** and **fetal ultrasound images**. The project explores Machine Learning and Deep Learning techniques to classify fetal health conditions using different types of medical data.

The project consists of three independent Jupyter notebooks covering **CTG-based classification, fetal brain ultrasound classification, and fetal kidney ultrasound classification**.

---

## 📌 Project Overview

Fetal health monitoring plays an important role in identifying potential complications during pregnancy.

This project investigates different Artificial Intelligence approaches for fetal health classification using:

* 📊 **Cardiotocography (CTG) data**
* 🧠 **Fetal brain ultrasound images**
* 🫘 **Fetal kidney ultrasound images**

Machine Learning algorithms are applied to CTG tabular data, while Deep Learning techniques are used to classify fetal ultrasound images.

---

## ✨ Project Components

### 1. 📊 CTG Classification

The `CTG.ipynb` notebook focuses on classifying fetal health using Cardiotocography data.

The notebook includes:

* Loading and exploring the CTG dataset
* Data preprocessing
* Feature analysis
* Feature selection
* Training Machine Learning models
* Model comparison
* Performance evaluation
* Confusion matrix and classification metrics

The Machine Learning models explored include:

* Logistic Regression
* Decision Tree
* Random Forest

The original CTG classification consists of three fetal health categories:

```text
1 → Normal
2 → Suspect
3 → Pathological
```

---

### 2. 🧠 Fetal Brain Classification

The `Fetal Brain.ipynb` notebook focuses on classification of fetal brain ultrasound images.

A Deep Learning-based image classification approach is used to distinguish between:

```text
Normal
   ↓
Abnormal
```

The notebook covers the image-based classification workflow, including image preprocessing, model training, validation, and prediction.

---

### 3. 🫘 Fetal Kidney Classification

The `Fetal_kidney.ipynb` notebook focuses on fetal kidney ultrasound image classification.

The model learns visual patterns from fetal kidney ultrasound images to classify them into:

```text
Normal
   ↓
Abnormal
```

The notebook contains the image preprocessing, Deep Learning model training, validation, and classification workflow.

---

## 🏗️ Overall Project Workflow

```text
                 Fetal Health Classification System
                              │
             ┌────────────────┼────────────────┐
             │                │                │
             ▼                ▼                ▼
         CTG Data       Brain Ultrasound   Kidney Ultrasound
             │                │                │
             ▼                ▼                ▼
       Preprocessing     Image Processing   Image Processing
             │                │                │
             ▼                ▼                ▼
     Machine Learning    Deep Learning     Deep Learning
             │                │                │
             ▼                ▼                ▼
       CTG Prediction    Brain Prediction   Kidney Prediction
             │                │                │
             └────────────────┼────────────────┘
                              ▼
                    Fetal Health Assessment
```

---

## 📂 Repository Structure

The current repository contains three Jupyter notebooks:

```text
Fetal-Health-Classification-System/
│
├── CTG.ipynb
├── Fetal Brain.ipynb
├── Fetal_kidney.ipynb
└── README.md
```

### Notebook Description

| File                 | Description                                                      |
| -------------------- | ---------------------------------------------------------------- |
| `CTG.ipynb`          | Fetal health classification using CTG data and Machine Learning  |
| `Fetal Brain.ipynb`  | Fetal brain ultrasound image classification using Deep Learning  |
| `Fetal_kidney.ipynb` | Fetal kidney ultrasound image classification using Deep Learning |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **TensorFlow / Keras**
* **Matplotlib**
* **Seaborn**
* **Machine Learning**
* **Deep Learning**
* **Computer Vision**

---

## 📊 Machine Learning

The CTG notebook explores and compares multiple Machine Learning algorithms:

### Logistic Regression

A linear classification algorithm used as a baseline model for fetal health classification.

### Decision Tree

A tree-based model that makes predictions through a sequence of feature-based decisions.

### Random Forest

An ensemble Machine Learning algorithm that combines multiple decision trees to improve classification performance.

The models are evaluated using metrics such as:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## 🧠 Deep Learning

The fetal brain and kidney notebooks use Deep Learning techniques for medical image classification.

The general workflow is:

```text
Ultrasound Dataset
       ↓
Image Preprocessing
       ↓
Training / Validation Split
       ↓
CNN / Deep Learning Model
       ↓
Model Training
       ↓
Validation
       ↓
Normal / Abnormal Prediction
```

---

## 🎯 Key Features

* Classification of fetal health using CTG data
* Comparison of multiple Machine Learning algorithms
* Fetal brain ultrasound image classification
* Fetal kidney ultrasound image classification
* Application of Deep Learning to medical images
* Model performance evaluation
* Multi-modal approach using both tabular and image-based medical data

---

## 🚀 Future Improvements

The project can be further extended by:

* Combining CTG, brain, and kidney predictions into a single unified model
* Developing a web-based interface for predictions
* Deploying the trained models using FastAPI or Flask
* Adding explainable AI techniques such as Grad-CAM
* Using advanced CNN architectures such as ResNet or EfficientNet
* Increasing dataset size and diversity
* Adding automated AI-generated reports
* Developing a real-time medical image prediction system

---

## ⚠️ Disclaimer

This project is intended for **educational and research purposes only**.

The predictions produced by these models should not be considered a medical diagnosis or a replacement for evaluation by qualified healthcare professionals.

---

## 👨‍💻 Author

**Abdul Touheed**

Computer Science Engineer | Machine Learning Enthusiast | Python Developer

---

## 📄 License

This project is intended for educational and research purposes.
