# 🌊 Automated Micro-Seismic Waveform 1D-CNN Classifier

A PyTorch 1D Convolutional Neural Network (CNN) designed to automate acoustic waveform processing, filtering noise and detecting micro-seismic event arrivals from continuous signal arrays.

---

## 📌 Executive Summary

* **1D-CNN Feature Extractor:** Architected a deep 1D Convolutional network with sequential Conv1D, Batch Normalization, and Max Pooling layers to extract temporal features directly from raw 1D signal windows.
* **Trace Segmentation:** Windowed continuous 360 Hz signal streams into 180-sample trace windows (0.5s intervals) to classify baseline noise, P-wave arrivals, and high-energy micro-seismic events.
* **Performance:** Achieved an **80.67% overall classification accuracy**, with an **0.88 F1-score** on primary signal arrivals.

---

## 📊 Performance Metrics

| Event Class | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| **Baseline Noise** | 0.70 | 0.70 | 0.70 | 10 |
| **P-Wave Arrival** | **0.84** | **0.92** | **0.88** | 111 |
| **Micro-Seismic Event** | 0.67 | 0.41 | 0.51 | 29 |
| **Overall Accuracy** | — | — | **80.67%** | **150** |

---

## 🛠️ Tech Stack

* **Framework:** PyTorch (Torch Tensors, DataLoader)
* **Signal Processing:** `scipy.datasets`, `numpy`
* **Evaluation & Diagnostics:** `scikit-learn`, `seaborn`, `matplotlib`
