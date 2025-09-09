# 🌊 Flood Area Segmentation with U-Net

## 📌 Overview
This project demonstrates **flood area detection using image segmentation** powered by the **U-Net architecture**.  
By segmenting satellite images into flooded vs non-flooded regions, we can provide actionable insights for **disaster management, insurance, and urban planning**.

---

## 🎯 Problem Statement
Floods are devastating natural disasters that affect millions of people each year.  
Traditional ground surveys are time-consuming and resource-intensive. Using **deep learning on aerial/satellite images** allows rapid, scalable, and automated flood detection.

---

## 🧠 Approach: U-Net Model
We implement a **U-Net CNN** from scratch using TensorFlow/Keras.  

**Key features:**
- Encoder (down-sampling): feature extraction with convolution + pooling.  
- Bottleneck: high-level feature representation.  
- Decoder (up-sampling): reconstructs segmentation map using transposed convolutions.  
- Skip connections: preserve spatial details.  

---

## 🗂️ Dataset
- Input images: satellite/aerial flood region images.  
- Ground-truth masks: binary masks marking flood zones.  
- Preprocessing:
  - Resize to **256×256**.  
  - Normalize to [0, 1].  
  - Masks reshaped to (H, W, 1).  

Dataset split:  
- **Training** → 70%  
- **Validation** → 15%  
- **Test** → 15%  

---

## ⚙️ Dependencies
Install with:

```bash
pip install numpy opencv-python matplotlib scikit-learn tensorflow
```

---

## 🚀 How to Run
1. Upload the dataset (`.zip`) and extract it into the notebook environment.  
2. Open and run `Flood_Area_Segmentation_Using_U_NET_Architecture.ipynb`.  
3. Steps included in the notebook:
   - Dataset loading and preprocessing.  
   - Visualization of image-mask pairs.  
   - Splitting data into train/validation/test sets.  
   - Building U-Net model.  
   - Training and evaluation.  
   - Visualization of predictions.  

---

## 📊 Training & Results

### 📈 Training Performance
- Epochs: **30**  
- Batch size: **8**  
- Optimizer: Adam  
- Loss function: Binary Crossentropy  
- Metrics: Accuracy  

**Observed Trends (sample run):**
- Final Training Accuracy: ~0.89  
- Final Validation Accuracy: ~0.88  
- Training Loss: steadily decreasing over epochs.  
- Validation Loss: stable after ~20 epochs.  
<img width="993" height="374" alt="image" src="https://github.com/user-attachments/assets/c684a272-7fb2-49f7-bca6-96f988349931" />

### 🖼️ Example Segmentation Results
| Input Image | Ground Truth Mask | Predicted Mask |
<img width="950" height="315" alt="image" src="https://github.com/user-attachments/assets/37479ed3-cd57-4e9c-ba5d-ce36af6bc636" />
<img width="950" height="315" alt="image" src="https://github.com/user-attachments/assets/fff9c201-898d-4575-af2f-f61f433f101e" />
<img width="950" height="315" alt="image" src="https://github.com/user-attachments/assets/c272d73d-d7e7-4266-b813-6001020d2348" />

---

## 🔮 Future Improvements
- Use **transfer learning encoders** (ResNet, EfficientNet) for better accuracy.  
- Apply **data augmentation** to increase robustness.  
- Post-processing (morphological operations) to refine boundaries.  
- Deployment using **Streamlit or Flask** for interactive flood prediction apps.  

---

## 📂 Repository Structure
```
├── Flood_Area_Segmentation_Using_U_NET_Architecture.ipynb  # Main notebook
└── README.md                                               # Project documentation
```

---

## 👨‍💻 Author
Developed as part of a **Deep Learning project on Flood Segmentation** using U-Net architecture.  
