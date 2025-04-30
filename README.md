# 🌄 HDR Reconstruction with Deep Learning - Leave Darkness, Light Up Reality

**A deep learning project for reconstructing HDR images from single-exposure LDR inputs using optimized preprocessing and network structures.**

---

## 📘 Project Overview

This project was developed for the College of Science and Engineering Research Competition, focusing on reconstructing **High Dynamic Range (HDR)** images from **Standard Dynamic Range (LDR)** inputs using machine learning techniques.

With HDR-capable displays and cameras becoming more common, this research explores ways to bridge the gap between legacy LDR data and modern HDR visualization needs. We improve upon existing HDRCNN-based architectures by integrating dataset preprocessing techniques, optimizing training performance, and testing alternative models such as **ResNet50**, **HDRUNet**, and **ExpandNet**.

---

## 🎯 Objectives

- Reconstruct HDR images from a single LDR input using CNNs
- Apply various preprocessing techniques to enhance dataset diversity
- Improve training speed and quality via mixed precision and dynamic learning rate
- Compare performance of different models (VGG16, ResNet50, HDRUNet, ExpandNet)

---

## 🛠️ Techniques Used

| Category               | Tools/Methods                                  |
|------------------------|------------------------------------------------|
| Framework              | PyTorch                                        |
| Baseline Model         | HDRCNN (VGG16)                                 |
| Optimization           | ResNet50, Mixed Precision, Dynamic LR         |
| Preprocessing          | Unsharp Mask, Gaussian Blur, Noise Reduction, Brightness/Contrast Adjustment |
| Evaluation Metrics     | PSNR, SSIM                                     |
| Dataset                | SI-HDR Dataset (Canon 5D Mark III, real-world exposure settings) |

---

## 🔍 Key Contributions

- Developed three dataset variations with diverse preprocessing strategies to test reconstruction performance
- Replaced VGG16 with **ResNet50**, reducing training time from 7h56m to 4h51m and increasing SSIM from 0.27 to 0.85
- Compared results with **HDRUNet** and **ExpandNet**; our modified HDRCNN showed better balance between performance and speed
- Enabled training on common hardware (RTX 3060 Ti), promoting local model usage and mobile NPU deployment potential

---

## 📊 Results Summary

| Model         | PSNR (dB) | SSIM   | Training Time |
|---------------|-----------|--------|----------------|
| HDRCNN (VGG16) | 13.01     | 0.2705 | 7h56m          |
| HDRCNN (ResNet50) | 16.08     | 0.8512 | 4h51m          |
| HDRUNet       | 21.25     | 0.661  | 3d14h32m       |
| ExpandNet     | 7.26      | 0.3022 | 19h21m         |

---

## 📷 Sample Comparison

| Model        | Output Preview |
|--------------|----------------|
| Ground Truth | ![](samples/gt.png) |
| Our HDRCNN (ResNet50) | ![](samples/ours.png) |
| HDRUNet      | ![](samples/hdrunet.png) |
| ExpandNet    | ![](samples/expandnet.png) |

---

## 🧠 Future Work

- Explore **multi-task learning** to integrate preprocessing directly into the model
- Apply **super-resolution** as a post-processing step for finer detail enhancement
- Expand training to support larger image resolutions and dynamic scene adaptation

---

## 👩‍💻 Authors

- **CHEN, PEI-CHI**
- **HO, TING-WEI**

---

## 📚 Citation

If you reference this work, please cite:

> CHEN, P.-C. & HO, T.-W. *HDR Reconstruction with Deep Learning: Dataset Preprocessing and Model Optimization*. College of Science & Engineering Research Competition, 2025.

---

## 📬 Contact

For inquiries or collaboration, please contact:  
📧 **peichi.dev@gmail.com**

---
