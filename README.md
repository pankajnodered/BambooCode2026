# 🌿 BambooLeafDS2026: Enhanced Latent Diffusion for Bamboo Leaf Disease Classification

## 📌 Overview

This repository presents our research work on **Bamboo Leaf Disease Classification** using deep learning and generative models.
We propose an **Enhanced Latent Diffusion Model** for data augmentation and compare its effectiveness with:

* Original dataset
* Traditional augmentation
* Vanilla LDM augmentation
* Enhanced LDM augmentation

The study evaluates multiple deep learning architectures under a **5-Fold Cross Validation + Bayesian Optimization** framework.

---

## 📂 Dataset

**BambooLeafDS2026**

The dataset contains bamboo leaf images categorized into multiple disease classes. It is organized into:

```
train/
val/
test/
```

* ✔ Train + Validation → used for 5-Fold CV
* ✔ Test → kept completely unseen for final evaluation

---

## 🧪 Experimental Setup

* 🔁 **5-Fold Stratified Cross Validation**
* 🔍 **Bayesian Optimization (Keras Tuner)**
* ❌ No data leakage
* 🔒 Fixed test set for final evaluation
* 📊 Evaluation Metrics:

  * Accuracy
  * Classification Report
  * Statistical Tests (Friedman, Wilcoxon)

---

## 📁 Repository Structure

### 🔬 Diffusion Models

#### 📄 `EnhancedLDMBamboo.ipynb`

* Implements **Enhanced Latent Diffusion Model **
* Improvements over vanilla LDM:

  * Better latent representation
  * Improved sample quality
* Used for generating **high-quality augmented images**

---

#### 📄 `VanillaLDMBamboo.ipynb`

* Standard Latent Diffusion Model implementation
* Baseline for comparison with Enhanced LDM

---

### 🤖 Classifier Pipelines

All classifier files follow:

* ✔ 5-Fold CV on (Train + Val)
* ✔ Bayesian Optimization
* ✔ Fixed test set

---

#### 📄 `classifiernoaug5cvbayesian.ipynb`

* Training on **original dataset only**
* ❌ No augmentation
* Baseline performance

---

#### 📄 `classifierstradaug5cvbayesian.ipynb`

* Uses **traditional augmentation**:

  * Rotation
  * Flipping
  * Zoom
  * Translation
* Evaluates classical augmentation impact

---

#### 📄 `classifiersvanillaldm5cvbayesian.ipynb`

* Training with **Vanilla LDM generated samples**
* Compares generative augmentation vs traditional

---

#### 📄 `classifierenhancedldm5cvbayesian.ipynb`

* Training with **Enhanced LDM generated samples**
* Final proposed method
* Expected best performance

---

## 🧠 Models Used

We evaluated multiple architectures:

* AlexNet
* VGG19
* ResNet50
* MobileNetV1
* DenseNet201
* EfficientNetB0
* Xception
* InceptionV4
* Vision Transformer (ViT-B16)

---

## 📊 Experimental Comparison

| Setup           | Description                 |
| --------------- | --------------------------- |
| Original        | No augmentation             |
| Traditional Aug | Flip, rotation, zoom        |
| Vanilla LDM     | Generated synthetic samples |
| Enhanced LDM    | Proposed method             |

---

## 🎯 Key Contributions

* ✅ Novel **Enhanced Latent Diffusion Model (E-LDM)**
* ✅ Comprehensive comparison across **9 architectures**
* ✅ Integration of **Bayesian Optimization**
* ✅ Robust evaluation using **5-Fold Cross Validation**
* ✅ Explainability using **Grad-CAM**

---

## 📈 Results (Summary)

* Enhanced LDM consistently outperforms:

  * Traditional augmentation
  * Vanilla LDM
* Improves classifier generalization
* Produces more realistic samples

---

## ⚙️ Requirements

Install dependencies:

```bash
pip install tensorflow keras opencv-python numpy scikit-learn keras-tuner vit-keras keras-applications
```

---

## 🚀 How to Run

1. Train diffusion model:

   * `EnhancedLDMBamboo.ipynb`
   * `VanillaLDMBamboo.ipynb`

2. Generate augmented dataset

3. Run classifiers:

   * No Aug → `classifiernoaug5cvbayesian.ipynb`
   * Traditional Aug → `classifierstradaug5cvbayesian.ipynb`
   * Vanilla LDM → `classifiersvanillaldm5cvbayesian.ipynb`
   * Enhanced LDM → `classifierenhancedldm5cvbayesian.ipynb`

---

## 📌 Reproducibility

* Random seed fixed
* Same evaluation protocol across all models
* Test set strictly held out

---

## 📜 Citation

If you use this work, please cite:

for Dataset
@article{bamboo2026,
  title={Enhanced Latent Diffusion Model for Bamboo Leaf Disease Classification},
  author={Pankajkumar Thakre, Jagdish Chakole},
  year={2026}
}
```

---

## 🤝 Acknowledgment

* TensorFlow & Keras
* Diffusion Model community
* Bamboo disease dataset contributors

---

## 📬 Contact

For queries or collaboration:

* 📧 Your Email
* 🌐 Your Institution

---
