# pothole_detection  (file is too big to share in github)
colab link : (https://colab.research.google.com/drive/1of3y62FiRDC4ldTjxqsAzPUd7xTG4bOt?usp=sharing)
# 🛣️ Pothole Detection using YOLOv8 Segmentation

This project implements an AI-based solution for automatic pothole detection and segmentation using the **YOLOv8-nano segmentation model**. Developed during an internship at **IIT Guwahati, Signal Processing Lab**, the model is designed for real-time performance and practical deployment in road safety and infrastructure maintenance systems.

## 📌 Objective

- Accurately detect and segment potholes in diverse road environments.
- Deliver real-time inference speeds suitable for video stream processing.
- Develop a scalable, cost-effective pipeline for smart infrastructure monitoring.

---

## 🔧 Technology Stack

- **Model**: YOLOv8-nano (Segmentation variant)
- **Language**: Python
- **Framework**: Ultralytics YOLOv8 (PyTorch-based)
- **Environment**: Google Colab (NVIDIA Tesla T4 GPU)
- **Libraries**: OpenCV, NumPy, Pandas, Matplotlib, Seaborn, Pillow, PyYAML

---

## 📁 Dataset

- **Source**: [Kaggle - Pothole Image Segmentation Dataset](https://www.kaggle.com/datasets/farzadnekouei/pothole-image-segmentation-dataset)
- **Total Images**: 780
  - Training: 720
  - Validation: 60
- **Annotation Format**: YOLOv8-compatible segmentation masks
- **Diversity**: Urban/rural roads, varied lighting (day, dusk), pothole types (shallow, deep, irregular)

---

## 🧠 Methodology

### 1. Dataset Preparation
- Auto-orientation and resizing to 640×640
- Augmentation: flipping, cropping, rotation, brightness & exposure adjustment
- YAML config for seamless training pipeline integration

### 2. Model Training
- Pretrained YOLOv8n-seg.pt weights
- 150 epochs, batch size 16
- Dropout: 0.25 | Learning rate: 0.0001 → 0.01
- Early stopping with patience=15

### 3. Inference Pipeline
- Frame-wise video processing using OpenCV
- Outputs annotated MP4s with pothole masks
- Real-time speed: ~10.9 ms/frame (~90 fps)

---

## 📈 Results

| Metric        | Value |
|---------------|-------|
| Precision     | 0.88  |
| Recall        | 0.85  |
| mAP@0.5       | 0.87  |

- **Inference Speed**: ~90 fps (on Tesla T4 GPU)
- **Output**: Real-time annotated videos/images

---

## 🖼️ Sample Output

![Sample](![final_output](https://github.com/user-attachments/assets/3cd1b46e-fa7d-4ded-8db7-15644f88324b)
)  
*Detected and segmented potholes from a video stream*

---

## ⚠️ Challenges Faced

- Dataset diversity (e.g., lack of night/wet road images)
- Segmentation accuracy in shadows and complex textures
- Limited GPU memory on Google Colab
- Real-time constraints for video inference

---

## 🚀 Future Work

- Deployment on edge/mobile devices (e.g., Jetson Nano, smartphones)
- GPS/GIS integration for pothole mapping
- Real-time alerts for smart city applications

---

## 🤝 Acknowledgements

- **Dataset**: [Farzad Nekouei, Kaggle](https://www.kaggle.com/datasets/farzadnekouei/pothole-image-segmentation-dataset)
- **Framework**: [Ultralytics YOLOv8](https://docs.ultralytics.com)

---

## 📄 License

This project is open-sourced under the [MIT License](LICENSE).

---

## 📬 Contact

For questions or collaboration, feel free to reach out:  
**Rithika Bollapragada**  
Email: [rithikapersonal706@gmail.com]  
LinkedIn: [www.linkedin.com/in/rithika-bollapragada-1419b325b)

