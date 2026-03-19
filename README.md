# brain-tumor-detection-and-classification-resnet50
Deep learning model for brain tumor detection and classification from MRI images using ResNet50 transfer learning (TensorFlow/Keras).

---

## Overview

Brain tumors are critical medical conditions that require early and accurate diagnosis. This project uses a Convolutional Neural Network (CNN) based on ResNet50 to automatically classify MRI images into different tumor categories.

---

## Classes

The model classifies MRI images into four categories:

- Glioma Tumor  
- Meningioma Tumor  
- Pituitary Tumor  
- No Tumor  

---

## Model Architecture

- Base Model: **ResNet50 (pretrained on ImageNet)**
- Custom Layers:
  - Flatten
  - Dense (128, ReLU)
  - Dense (64, ReLU)
  - Output Layer (Softmax - 4 classes)

---

## Dataset

The dataset used in this project is sourced from Kaggle:

https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

Note:
The model was trained on an earlier version of this dataset. The dataset may have been updated since the time of training, which may result in slight variations in results if retrained.

---

## Training Details

- Image Size: 224 × 224  
- Batch Size: 32  
- Optimizer: Adam  
- Loss Function: Categorical Crossentropy  
- Epochs Trained: 20  
- Best Model Selected at: **Epoch 17 (based on validation performance)**  

---

## Results

### Accuracy & Loss
- Training Accuracy: ~83%  
- Validation Accuracy: ~77%  
- Validation Loss: ~0.4–0.5  

### Confusion Matrix
Model shows some confusion between tumor classes, especially Glioma and Meningioma.

### Classification Metrics
- Precision, Recall, and F1-score indicate moderate performance across classes.

### ROC Curve
- AUC values range between **0.51 – 0.56**

---

## Project Structure

brain-tumor-detection-and-classification-resnet50
├── brain_tumor_resnet50_code.ipynb
├── results/
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── accuracy_loss.png
└── README.md

---

## Note

- The trained model file (`.h5`) is not included due to GitHub size limitations.
- Dataset is also not uploaded .

---

## Future Improvements

- Fine-tuning ResNet50 layers  
- Data augmentation  
- Using advanced architectures (EfficientNet, DenseNet)  
- Hyperparameter tuning  
- Grad-CAM visualization for interpretability  

---

## Technologies Used

- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  
- Scikit-learn  

---

## Author

**Arun Karthik R**  
B.Tech Automation and Robotics Engineering  

---

## Acknowledgment

This project is developed for learning and exploring deep learning applications in medical image analysis.
