# Skin-Cancer-and-Pneumonia-Detection
# 🧠 Medical Image Classification using Deep Learning  

## 📌 Project Overview  
This project applies **Deep Learning** for medical image classification on two different datasets:  

1. **Skin Cancer Detection** – using the **ISIC Skin Cancer Dataset** with Transfer Learning (ResNet50).  
2. **Pneumonia Detection** – using the **Chest X-Ray Images Dataset** (Kaggle) with a custom CNN.  

The goal is to build accurate models for **binary classification (disease vs. healthy)** using both **Transfer Learning** and **custom CNNs**.  

---

## 🗂️ Datasets  

### 🔹 Skin Cancer Detection  
- Dataset: [ISIC Skin Cancer Dataset](https://www.isic-archive.com/)  
- Subset: 500–1000 images  
- Preprocessing:  
  - Resize images to **128×128**  
  - Normalize pixel values to `[0,1]`  

### 🔹 Pneumonia Detection  
- Dataset: [Chest X-Ray Images Dataset (Kaggle)](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia)  
- Subset: Sample images from dataset  
- Preprocessing:  
  - Resize to **128×128**  
  - Normalize pixel values to `[0,1]`  

---

## 🏗️ Model Architectures  

### 🔹 Skin Cancer Detection (Transfer Learning – ResNet50)  
- Pre-trained **ResNet50** (ImageNet weights)  
- Removed top layers (`include_top=False`)  
- Added: Global Average Pooling + Dense layers  
- Final Dense (Sigmoid) for binary classification  
- Optimizer: **Adam (1e-4)**  
- Loss: **Binary Crossentropy**  

### 🔹 Pneumonia Detection (Custom CNN)  
- 2 Convolutional layers with ReLU + MaxPooling  
- Flatten + Dense layers  
- Final Sigmoid output  
- Optimizer: **Adam**  
- Loss: **Binary Crossentropy**  

---

## 📊 Training Setup  
- **Batch Size:** 32  
- **Epochs:** 8–12  
- **Evaluation Metrics:** Accuracy & ROC Curve  

---

## ✅ Results  

### 🔹 Skin Cancer Detection  
- Transfer Learning with ResNet50 achieved **high accuracy** on validation set.  
- Prevented overfitting using Dropout & Frozen Base Layers.  

📈 *(ROC Graphs )*  
<img width="820" height="651" alt="image" src="https://github.com/user-attachments/assets/51fa75c6-0847-44b3-90eb-9fcf7f3946cb" />

---

### 🔹 Pneumonia Detection  
- Simple CNN provided **reasonable accuracy** with fewer layers.  
- Evaluated using **Accuracy and ROC Curve**.  

📉 *( Accuracy/Loss Graphs + ROC Curve )*  
<img width="900" height="417" alt="image" src="https://github.com/user-attachments/assets/50f0344e-a6fe-4100-a0f7-364445d422e0" />
<img width="770" height="665" alt="image" src="https://github.com/user-attachments/assets/69a11b37-e9e0-4612-9e9c-dc68be1be478" />

---

## 🚀 How to Run  

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/medical-image-classification.git
   cd medical-image-classification
