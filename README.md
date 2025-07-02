# 🩺 ECG-Image-Compression

This repository contains the codebase for the Final Year Project titled:

**"Comparative Research on ECG Image Compression: Assessing Diagnostic Integrity"**

The goal of this project is to explore and compare different image compression techniques for ECG paper images, focusing on preserving diagnostic accuracy while improving storage efficiency.

---

## 📦 Compression Techniques Implemented

This project investigates **three base compression methods**:

- 📉 **Discrete Wavelet Transform (DWT)**
- 🤖 **Convolutional Autoencoder (CAE)**
- 🧠 **Context-Adaptive Lossless Image Compression (CALIC)**

To enhance compression performance, **entropy coding techniques** are combined with these base methods:

- 🗜️ **Huffman Coding (HC)**
- 🧮 **Arithmetic Coding (AC)**

### 🔧 Final Compression Variants Compared

| Method             | Description                                      |
|--------------------|--------------------------------------------------|
| DWT                | Wavelet-based lossy compression                  |
| DWT + HC           | DWT followed by Huffman Coding                   |
| DWT + AC           | DWT followed by Arithmetic Coding                |
| CAE                | Deep learning-based lossy compression            |
| CAE + HC           | CAE followed by Huffman Coding                   |
| CAE + AC           | CAE followed by Arithmetic Coding                |
| CALIC              | Context-adaptive lossless compression            |
| CALIC + HC         | CALIC with Huffman Coding                        |
| CALIC + AC         | CALIC with Arithmetic Coding                     |

---

## 📂 Dataset

The ECG image dataset used in this study is derived from the **MIT-BIH Arrhythmia Database**.  
Each ECG signal was first visualized as a 2D image, then resized and preprocessed before applying the compression methods.

---

## ⚙️ Preprocessing Steps

1. **Read Data**: Load raw ECG waveform images.
2. **Resize**: Standardize all images to a fixed size.
3. **Apply Compression**: Use one of the selected methods listed above.
4. **Evaluate Results**.

---

## 📈 Performance Metrics

Each compression method was evaluated based on the following metrics:

- 📏 **Compression Ratio (CR)** – Ratio of original to compressed size.
- 📊 **Peak Signal-to-Noise Ratio (PSNR)** – Image quality after compression.
- 🧠 **Structural Similarity Index (SSIM)** – Structural similarity to the original.
- 📉 **Percentage Root Mean Square Difference (PRD)** – Diagnostic distortion measure.
- ⏱ **Processing Time** – Time taken for compression and decompression.

---
## 📊 Results Overview
- CR
- ![image](https://github.com/user-attachments/assets/5862e6b5-4af7-493a-832c-e65371bcfaca)

## 🚀 Getting Started

### Requirements

- Python 3.8+
- NumPy
- OpenCV (`cv2`)
- PyTorch (for CAE)
- PyWavelets (for DWT)
- PIL (Pillow)
- Custom Huffman and Arithmetic coding modules

### Installation

```bash
git clone https://github.com/jiawei0304/ECG-Image-Compression.git
cd ECG-Image-Compression
pip install -r requirements.txt
