# Exploring-GAN-Variants-for-Balancing-Imbalanced-Datasets

## 📌 Project Overview
This project explores the use of **Generative Adversarial Networks (GANs)** to address class imbalance in the FER2013 (Facial Expression Recognition) dataset. Specifically, we focus on the "disgust" class, which is significantly underrepresented. We implement and compare **Vanilla GAN** and **DCGAN** to generate synthetic samples and evaluate their impact on a CNN classifier.

## 📊 Dataset: FER2013
- **Source:** Kaggle (msambare/fer2013): https://www.kaggle.com/datasets/msambare/fer2013
- **Target Class:** "Disgust" (Minority class)
- **Problem:** The severe imbalance leads to low recall and F1-scores for minority emotions.



## 🛠️ Methodology
1. **Baseline:** Train a CNN classifier on the original imbalanced data.
2. **Vanilla GAN Augmentation:** Generate synthetic "disgust" images using a fully connected GAN and retrain the classifier.
3. **DCGAN Augmentation:** Generate synthetic "disgust" images using Deep Convolutional GANs and retrain the classifier.

## 🚀 Results & Comparison
The introduction of GAN-generated data consistently improved the recall for the minority class.

| Model Variant | Accuracy | Disgust Precision | Disgust Recall | Disgust F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| Baseline | ~70% | 0.75 | 0.30 | 0.32 |
| Vanilla GAN Augment | ~90% | 0.78 | 0.41 | 0.54 |
| **DCGAN Augment (Best)** | **~91%** | **0.88** | **0.41** | **0.56** |

### Key Observation:
While Vanilla GANs provided a good baseline, **DCGAN** produced higher quality spatial features, leading to a significant jump in Recall (0.88), proving that even slightly blurry synthetic images help the model generalize better to rare classes.



## 📁 Repository Structure
- `Special_Topics_Project.ipynb(4)`: Full implementation (Data prep, GAN training, Classification).
- Note: It was runned using Google Colab
- `Project_Report.pdf`: Detailed analysis and theoretical background.
