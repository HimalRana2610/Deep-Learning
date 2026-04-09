# 🧠 Deep Learning-Based GI Disease Classification with Explainability

## 📌 Overview

This project focuses on classification of gastrointestinal (GI) diseases using deep learning on Wireless Capsule Endoscopy (WCE) images.

It addresses a critical challenge in medical AI — class imbalance — and introduces novel enhancements such as:

- Focal Loss for imbalance handling
- Ensemble learning for improved accuracy
- Grad-CAM for model explainability

---

## 🎯 Objectives

- Classify GI diseases from endoscopy images
- Handle imbalanced datasets effectively
- Improve performance using transfer learning
- Provide visual explanations of model predictions

---

## 📂 Dataset

- Dataset is stored in:
```
Data/
 ├── ampulla_of_vater/
 ├── angiectasia/
 ├── blood_fresh/
 ├── blood_hematin/
 ├── erosion/
 ├── erythema/
 ├── foreign_body/
 ├── ileocecal_valve/
 ├── lymphangiectasia/
 ├── normal_clean_mucosa/
 ├── polyp/
 ├── pylorus/
 ├── reduced_mucosal_view/
 ├── ulcer/
```
- Each folder represents a disease class
- Images are labeled based on folder names

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing

- Image resizing: `224 × 224`
- Normalization using ImageNet statistics
- Dataset split:
    - Train: 70%
    - Validation: 15%
    - Test: 15%

---

### 2️⃣ Handling Class Imbalance (Novelty)

We use Focal Loss instead of standard CrossEntropy Loss:
- Focuses more on hard/misclassified samples
- Reduces bias toward majority classes

---

### 3️⃣ Transfer Learning Models

We used pretrained models:
- EfficientNet-B0
- ResNet50
- MobileNetV2

Steps:
- Load ImageNet pretrained weights
- Freeze base layers
- Replace final classification layer

---

### 4️⃣ Ensemble Learning (Novelty)

Predictions from all three models are combined using:
- Soft Voting (Average Probability)

This improves:
- Accuracy
- Robustness

---

### 5️⃣ Explainability with Grad-CAM (Novelty)

We applied Grad-CAM to visualize:
- Which regions of the image influenced predictions
- Helps in medical interpretability

---

## 📊 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

## 🚀 Results

- Ensemble model outperforms individual models
- Focal Loss improves minority class prediction
- Grad-CAM provides meaningful visual insights

---

## 🛠️ Tech Stack

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- OpenCV
- tqdm

---

## ▶️ How to Run

### 1. Clone repository
```bash
git clone https://github.com/HimalRana2610/Deep-Learning.git
cd "Minor Project"
```

### 2. Install dependencies
```bash
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu130
pip install numpy matplotlib opencv-python pillow tqdm jupyterlab
```

### 3. Run Notebook
```bash
jupyter notebook
```

---

## 📁 Project Structure

```
├── Data/
├── app.ipynb
├── README.md
```

---

## 🌟 Key Contributions (Novelty)

- ✅ Focal Loss for imbalance handling
- ✅ Ensemble of 3 deep learning models
- ✅ Grad-CAM for explainable AI

---

## 📌 Future Work

- Use attention mechanisms (CBAM, SE blocks)
- Apply self-supervised learning
- Deploy model as a web application

---

## Authors

- Himal Rana
- Ankit Yadav

---

## 🎓 Acknowledgment

Guided by:
- Dr. Praveen Chandaliya

Department of AI, SVNIT

---

## 📜 License

This project is for academic and research purposes only.