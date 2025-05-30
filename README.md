# 📦 Warehouse Object Detection with YOLOv8

This project focuses on building an intelligent object detection system tailored for warehouse environments. It uses deep learning models to identify logistical elements like **pallets**, **stillage racks**, and **small load carriers** in real-time via camera surveillance.

## 🧰 Project Overview

Modern warehouses need constant monitoring of objects to ensure efficiency and safety. Manual monitoring is error-prone and inefficient. We propose an AI-powered surveillance system capable of real-time object detection using computer vision models like **YOLOv8** and **Faster R-CNN**.

---

## 🚀 Key Features

- 📷 Real-time object detection via camera feeds
- 🎯 Models trained on custom annotated datasets
- 🧪 Comparison between YOLOv8 and Faster R-CNN
- 🖥️ Final deployment using OpenCV and PyTorch
- ⚡ Lightweight and fast inference with YOLOv8
- 📊 Model evaluation using metrics like mAP, Precision, and Recall

---

## 📂 Dataset

- **Source**: Roboflow (Open-source)
- **Classes used**: `pallet`, `stillage`, `small_load_carrier`
- **Format**: YOLOv8 (TXT) & COCO (JSON)
- **Preprocessing**:
  - Rotation and resizing
  - Class balancing
  - Augmentation using Mosaic, HSV, Flip (via Albumentations)

---

## 🧠 Models Used

| Model        | Type               | Strength                    |
| ------------ | ------------------ | --------------------------- |
| YOLOv8       | One-stage detector | Real-time performance       |
| Faster R-CNN | Two-stage detector | Precision (low in our case) |

---

## ⚙️ Training Setup

- **YOLOv8**:

  - Epochs: 25
  - Batch size: 10
  - Image size: 416x416
  - Optimizer: SGD
  - Learning rate: 0.001

- **Faster R-CNN**:
  - Epochs: 25
  - Backbone: MobileNetV3
  - Optimizer: SGD
  - Learning rate: 0.005

---

## 📈 Evaluation Results

| Model        | mAP@0.5 | Precision | Recall |
| ------------ | ------- | --------- | ------ |
| YOLOv8       | 0.62    | 0.71      | 0.55   |
| Faster R-CNN | 0.02    | 0.30      | 0.20   |

📌 YOLOv8 is the final selected model due to its superior accuracy, speed, and deployment ease.

---

## 🔧 Deployment

- Integrated with **OpenCV** for real-time video feed processing
- Runs locally or can be embedded in smart surveillance cameras
- Annotated detections overlayed live on video frames

---

## 🛠️ Technologies

- Python 3.10
- PyTorch
- OpenCV
- Roboflow
- Ultralytics YOLOv8
- Albumentations
- Google Colab Pro+ (Training Environment)

## 📚 References

- [YOLOv8 by Ultralytics](https://github.com/ultralytics/ultralytics)
- [Fast R-CNN Paper](https://arxiv.org/abs/1504.08083)
- [Roboflow](https://roboflow.com)
- [PyTorch](https://pytorch.org)
- [OpenCV](https://opencv.org)
