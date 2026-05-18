# YOLO-DC: Robust Electric Bike Detection and Tracking in Critical Scenarios

This repository contains the official implementation of **YOLO-DC**, a specialized object detection model for electric bikes (E-bikes) in complex traffic scenarios, designed for Intelligent Transportation Systems (ITS) and Advanced Driver Assistance Systems (ADAS).

<img width="492" height="369" alt="image" src="https://github.com/user-attachments/assets/3a7eb8c6-2907-4c4a-a078-304a4470a047" />


---

## 📌 Overview
Electric bikes (E-bikes) present significant road safety challenges due to their high speeds and dynamic instability, requiring accurate, real-time detection in diverse conditions (low light, occlusion, bad weather, tilted perspectives). Existing YOLO-based detectors often struggle with these challenges, and dedicated E-bike datasets remain scarce.

To address these gaps, YOLO-DC enhances YOLOv8s with three key modifications:
- **Deformable Convolutional Network-v2 (DCNv2)** in the backbone for improved spatial adaptability
- **Convolutional Block Attention Module (CBAM)** in the neck for enhanced spatial-channel feature representation
- **Hybrid Intersection over Union (HIoU) loss** for optimized bounding box regression, especially for small objects

The model is validated on the custom **Electric Bikes Dataset (EBD)** and achieves significant improvements over the baseline YOLOv8s.


---

## ✨ Key Features
✅ Specialized E-bike detection model built on YOLOv8s  
✅ DCNv2-enhanced backbone for spatial adaptability in tilted/occluded scenarios  
✅ CBAM attention module to highlight critical features in complex environments  
✅ HIoU loss optimized for small-object detection (E-bikes)  
✅ +12.4% mAP@50 improvement over YOLOv8s on the EBD dataset  
✅ 98.4% overall detection accuracy in real-world traffic scenarios  
✅ Real-time performance for on-board deployment in ITS/ADAS  

---

## 📊 Results Highlights
Compared to the YOLOv8s baseline on the Electric Bikes Dataset (EBD):
- **mAP@50**: +12.4% improvement
- **Overall Detection Accuracy**: 98.4%
- **Real-Time Performance**: Suitable for intelligent driving systems

---

## 🚀 Getting Started

### Requirements
```bash
pip install -r requirements.txt
```

### Dataset
This work uses the **Electric Bikes Dataset (EBD)**, a custom dataset of 1,257+ real-world images capturing E-bikes under diverse conditions (low light, occlusion, bad weather, and tilted perspectives).  

<img width="288" height="161" alt="image" src="https://github.com/user-attachments/assets/9dd2d37c-058d-4325-aa2f-0992cc332909" />


**The dataset is available on request.** 
Please contact the author to obtain access.

### Training
```bash
python train.py --config config/yolo_dc.yaml --data ./data/ebd.yaml
```

### Inference
```bash
python detect.py --weights weights/yolo_dc_best.pt --source ./test_images/
```

---

## 📄 Citation
If you use this work in your research, please cite the original paper:
*(Add your paper citation here once published)*

```bibtex
@article{your_citation_key,
  title={YOLO-DC: Robust Electric Bike Detection and Tracking in Critical Scenarios},
  author={Tian, Jinxin and Ghaffar, Muhammad Arslan and Li, Zhaokai},
  journal={},
  volume={},
  number={},
  pages={},
  year={},
  publisher={}
}
```

---

## 📝 License
This project is released under the **CC BY 4.0 License**.

---

## Contact
For questions, dataset access, or issues, please contact:  
**Muhammad Arslan Ghaffar** – ghaffar@siat.ac.cn

