# Polyp & Stomach Ulcer Detection Model (BalancedDS)

## 📌 Overview
This project builds a **YOLO11L-based object detection model** to identify **polyps** and **stomach ulcers** from endoscopy images.  
To overcome dataset limitations, I created a **custom mixed dataset (BalancedDS)** by **combining multiple public sources** to ensure class balance and diversity.  
The pipeline includes **exploratory data analysis (EDA)**, **data preprocessing**, and **Randomized Controlled Tests (RCTs)** with **30 and 300 images** to validate the model’s performance across different scales.  

---

## 🛠️ Tech Stack
- **YOLO11L (Ultralytics)** for object detection  
- **Python** (PyTorch, OpenCV, Pandas, NumPy)  
- **Kaggle** for model training & evaluation  

---

## 📊 Dataset
- Source: [BalancedDS (Kaggle)](https://www.kaggle.com/datasets/varunrana3104/balancedds)  
- Type: Mixed dataset curated from **multiple sources**  
- Classes: **Polyp** and **Stomach Ulcer**  
- Balanced sampling applied to reduce bias  

---

## 🔍 Methodology
1. **EDA**
   - Class balance verification (Polyp vs Ulcer)  
   - Distribution of bounding box sizes  
   - Sample visualization and anomaly checks  

2. **Preprocessing**
   - Resizing & normalization  
   - Augmentations: rotations, flips, contrast adjustment  
   - Removal of duplicates & low-quality images  

3. **Model Training**
   - YOLO11L trained with hyperparameter tuning  
   - Loss function optimized for small object detection  

4. **Evaluation**
   - Standard test metrics (Precision, Recall, mAP)  
   - **RCT-30**: Controlled test with 30 images  
   - **RCT-300**: Larger, more diverse test set  

---

## 📈 Results

### YOLO11L Metrics (BalancedDS)
- **Precision (B):** `0.9222`  
- **Recall (B):** `0.8758`  
- **mAP@50 (B):** `0.9286`  
- **mAP@50-95 (B):** `0.6183`  
- **Fitness Score:** `0.6493`  

### RCT Validation
- **RCT-30 Accuracy:** ~92%  
- **RCT-300 Accuracy:** ~90%  

---

## 🚀 Features
- Custom **BalancedDS dataset** for reliable detection  
- Detects **polyps** and **ulcers** with high accuracy  
- Includes **EDA, preprocessing, and RCT-based testing**  
- Reproducible Kaggle workflow  

---

Polyp-Stomach-Ulcer-Detection-Model/
│── data/
│── eda_notebook.ipynb
│── preprocessing.ipynb
│── runs/
│── best.pt
│── detect.py
│── README.md


---

## ▶️ Usage
```bash
# Run inference on an endoscopy image
!yolo task=detect mode=predict model=best.pt source="endoscopy_sample.jpg"


## 📂 Project Structure
