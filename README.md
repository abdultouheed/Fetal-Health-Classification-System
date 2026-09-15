# 🩺 Fetal Health Classification System

An AI-driven healthcare system designed to assist in the **early identification of potential fetal abnormalities** using **Cardiotocography (CTG) data and fetal ultrasound images**.

The system combines traditional Machine Learning for CTG-based fetal health classification with Deep Learning-based image classification for fetal brain and kidney ultrasound images.

---

## 📌 Project Overview

Fetal health monitoring is important for identifying potential complications during pregnancy.

This project develops a multi-modal AI-based classification system that analyzes:

- 📊 **CTG data** for fetal health assessment
- 🧠 **Fetal brain ultrasound images** for abnormality classification
- 🫘 **Fetal kidney ultrasound images** for abnormality classification

The outputs from these models can be used together to provide an overall **Normal / Abnormal fetal health assessment**.

---

## ✨ Features

- 📊 CTG-based fetal health classification
- 🧠 Fetal brain ultrasound image classification
- 🫘 Fetal kidney ultrasound image classification
- 🤖 Comparison of multiple Machine Learning algorithms
- 🧠 Deep Learning-based image classification
- 🔄 Multi-modal fetal health assessment
- ⚡ Automated prediction of Normal / Abnormal cases
- 📈 Evaluation using classification metrics and confusion matrices

---

## 🏗️ System Architecture

```text
                    FETAL HEALTH CLASSIFICATION SYSTEM
                                │
             ┌──────────────────┴──────────────────┐
             │                                     │
             ▼                                     ▼
      CTG Tabular Data                       Ultrasound Images
             │                                     │
             ▼                           ┌─────────┴─────────┐
       Preprocessing                     │                   │
             │                           ▼                   ▼
             ▼                    Brain Ultrasound    Kidney Ultrasound
    Machine Learning                    │                   │
             │                           ▼                   ▼
     ┌───────┼────────┐            CNN Model           CNN Model
     │       │        │                │                   │
     ▼       ▼        ▼                ▼                   ▼
    LR      DT        RF           Brain Result       Kidney Result
     │       │        │                │                   │
     └───────┴────────┘                └─────────┬─────────┘
             │                                   │
             ▼                                   ▼
       CTG Prediction                    Image Predictions
             │                                   │
             └────────────────┬──────────────────┘
                              ▼
                    Final Health Assessment
                              │
                              ▼
                    Normal / Abnormal

.

📊 CTG Classification

The CTG dataset contains physiological measurements used to assess fetal condition.

The CTG pipeline includes:

CTG Dataset
     ↓
Data Preprocessing
     ↓
Feature Selection
     ↓
Train / Test Split
     ↓
Model Training
     ↓
Classification
     ↓
Fetal Health Prediction

The CTG model initially performs multi-class classification:

1 → Normal
2 → Suspect
3 → Pathological

These predictions can subsequently be interpreted as an overall:

Normal
   or
Abnormal

🧠 Fetal Brain Classification

A Deep Learning-based image classification model is used to analyze fetal brain ultrasound images.

Brain Ultrasound Image
          ↓
Image Preprocessing
          ↓
CNN Model
          ↓
Feature Extraction
          ↓
Classification
          ↓
Normal / Abnormal

The model learns visual patterns from fetal brain ultrasound images to distinguish between normal and abnormal cases.

🫘 Fetal Kidney Classification

A separate Deep Learning model is used for fetal kidney ultrasound image classification.

Kidney Ultrasound Image
          ↓
Image Preprocessing
          ↓
CNN Model
          ↓
Feature Extraction
          ↓
Classification
          ↓
Normal / Abnormal

This provides an additional source of information for fetal health assessment.

🔄 Multi-Modal Prediction

The project combines information from different medical data sources.

              ┌───────────────┐
              │   CTG Model   │
              └───────┬───────┘
                      │
                      ▼
                 CTG Result
                      │
                      │
┌─────────────────────┼─────────────────────┐
│                     │                     │
▼                     ▼                     ▼
Brain Model       Kidney Model         CTG Model
│                     │                     │
▼                     ▼                     ▼
Brain Result      Kidney Result        CTG Result
│                     │                     │
└─────────────────────┼─────────────────────┘
                      ▼
              Combined Assessment
                      │
                      ▼
              Normal / Abnormal

The multi-modal approach provides multiple perspectives for fetal health assessment instead of relying on a single data source.

🛠️ Technologies Used
Python
Pandas
NumPy
Scikit-learn
TensorFlow / Keras
Deep Learning
Convolutional Neural Networks (CNN)
Matplotlib
Seaborn

📂 Project Structure
Fetal-Health-Classification/
│
├── CTG/
│   ├── dataset/
│   │   └── fetal_health.csv
│   │
│   ├── preprocessing.py
│   ├── train.py
│   ├── predict.py
│   └── model/
│       ├── random_forest.pkl
│       └── scaler.pkl
│
├── Fetal-Brain/
│   ├── dataset/
│   │   ├── normal/
│   │   └── abnormal/
│   │
│   ├── train.py
│   └── predict.py
│
├── Fetal-Kidney/
│   ├── dataset/
│   │   ├── normal/
│   │   └── abnormal/
│   │
│   ├── train.py
│   └── predict.py
│
├── requirements.txt
└── README.md

The actual structure may vary depending on the final implementation.

⚙️ Installation
1. Clone the Repository
git clone https://github.com/your-username/fetal-health-classification.git
2. Navigate to the Project
cd fetal-health-classification
3. Create a Virtual Environment
python -m venv venv

Activate it on Windows:

venv\Scripts\activate

Linux/macOS:

source venv/bin/activate

4. Install Dependencies
pip install -r requirements.txt
▶️ Running the Project
CTG Prediction

Run the CTG prediction script:

python CTG/predict.py

Provide the required CTG features to obtain the predicted fetal health condition.

Brain Image Prediction
python Fetal-Brain/predict.py

Provide a fetal brain ultrasound image to obtain the prediction.

Kidney Image Prediction
python Fetal-Kidney/predict.py

Provide a fetal kidney ultrasound image to obtain the prediction.
