# GAN-based Data Augmentation for Class Imbalance in Facial Expression Recognition

## 📌 Project Overview
This project explores the use of Generative Adversarial Networks (GANs) to address class imbalance
in the FER2013 facial expression dataset. The focus is on the *disgust* class, which is significantly
underrepresented. Vanilla GAN and DCGAN models are implemented to generate synthetic samples, and
their impact is evaluated using a CNN classifier.

---

## 📊 Dataset: FER2013
- Source: Kaggle (msambare/fer2013)
- Classes: angry, disgust, fear, happy, neutral, sad, surprise
- Minority Class: *Disgust*
- Challenge: Severe class imbalance leading to poor minority class recall

---

## 🛠️ Methodology
- **Baseline:** CNN trained on the original imbalanced dataset
- **Vanilla GAN Augmentation:** Fully connected GAN used to generate synthetic *disgust* images
- **DCGAN Augmentation:** Convolutional GAN used to generate spatially consistent *disgust* images
- **Evaluation:** Classification report, confusion matrix, recall, and F1-score

---

## 🚀 Results & Comparison

| Model Variant | Accuracy | Disgust Precision | Disgust Recall | Disgust F1-score |
|--------------|----------|-------------------|----------------|------------------|
| Baseline (Imbalanced) | 0.56 | 0.73 | 0.22 | 0.33 |
| Vanilla GAN Augmented | 0.57 | 0.73 | 0.32 | 0.45 |
| DCGAN Augmented | 0.56 | 0.80 | 0.39 | 0.52 |

### Key Observations
- Overall accuracy remained relatively stable across experiments.
- GAN-based augmentation significantly improved minority class recall and F1-score.
- DCGAN produced the most balanced improvement, indicating higher-quality synthetic samples.
- Results show reduced bias toward majority classes despite imperfect image quality.

---

## 📁 Repository Structure
- `Special_Topics_Project.ipynb` – Full pipeline (data preprocessing, GAN training, classification)
- `Project_Report.pdf` – Detailed methodology, experiments, and analysis

> Note: Experiments were conducted using Google Colab.

