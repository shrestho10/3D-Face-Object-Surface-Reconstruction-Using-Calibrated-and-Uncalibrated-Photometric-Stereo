# 🧠 CS217 Final Project: Photometric Stereo — Calibrated & Uncalibrated

## 🎥 Demo & Code

- 🔗 **[🔍 View Demo](https://shrestho10.github.io/shagoto-mesh-website/)**  
- 📽️ **[🎬 Watch Video](https://youtu.be/5YFaPDeGGcs)**

---

## 📌 Overview

Photometric Stereo is a technique in computer vision to recover surface normals and reconstruct 3D shapes using images of an object taken under varying lighting conditions while keeping the camera fixed.

This project explores:
- **Calibrated Photometric Stereo** (known lighting directions)
- **Uncalibrated Photometric Stereo** (unknown lighting directions)

We implement analytical and deep learning-based methods and evaluate them on real datasets.

---

## 🎯 Objectives

### 🔹 Part 1: Calibrated Photometric Stereo
- Use grayscale images with **known light directions**
- Compute surface normals using the **Lambertian reflectance model**
- Reconstruct depth via **Frankot-Chellappa algorithm**
- Generate a 3D mesh using:
  - Grid-based triangulation, or
  - **Ball Pivoting Algorithm (BPA)**

### 🔹 Part 2: Uncalibrated Photometric Stereo
Estimate surface normals and shape using three different approaches:
1. **SVD-based factorization** (with GBR ambiguity)
2. **Simple CNN** trained on DiLiGenT dataset
3. **SDPS-Net**: Deep two-stage model  
   - LCNet: estimates lighting direction/intensity  
   - NENet: estimates surface normals  

---

## 📂 Datasets Used

### 🧑‍🦲 [Yale Face Database B](https://vision.ucsd.edu/content/yale-face-database)
- 10 subjects × 64 lighting conditions
- Used frontal pose images

### 📦 [DiLiGenT Benchmark](https://sites.google.com/view/photometricstereo/home)
- 10 objects × 96 lighting conditions
- Includes masks, ground-truth normals, and calibrated lighting

---

## 🛠️ Technical Approach

### 🔸 Calibrated Pipeline
1. **Lambertian Model**: \( I = \rho (N \cdot L) \)
2. Solve for \( x = \rho N \) using least squares
3. Extract **albedo** and **normals**
4. Reconstruct **depth map** via Frankot-Chellappa
5. Build 3D **mesh** from depth:
   - Option A: Triangulation
   - Option B: **Ball Pivoting Algorithm (BPA)**

### 🔸 Uncalibrated Modes
- **Mode 1**: SVD-based normal estimation  
- **Mode 2**: Simple CNN trained with cosine similarity loss  
- **Mode 3**: **SDPS-Net**  
  - LCNet (light classification)
  - NENet (normal regression)



## 👤 Author

**Shagoto Rahman**  
Ph.D. Student @ UCI  
CS 217: Final Project Report  
📧 shagotor@uci.edu

---

