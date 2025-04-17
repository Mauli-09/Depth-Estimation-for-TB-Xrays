# Depth-Estimation-for-TB-Xrays
Pseudo3D-TB-ChestXray

# 🫁 Tuberculosis X-ray in 3D — Pseudo-3D Visualization from a 2D Image using MiDaS

> “Can we give doctors and learners a 3D look at a TB-affected lung using just a flat X-ray?”  
> This project says — YES. ✨

---

## 🔍 Overview

This project transforms a **2D chest X-ray image with Tuberculosis (TB)** into a **pseudo-3D interactive visualization** using a deep learning model. The key idea is to simulate depth and highlight the TB-affected region for **intuitive understanding**, education, or assistive diagnosis.

We use:
- ✅ An open-source **MiDaS depth estimation model**
- ✅ **OpenCV** for bounding box labeling
- ✅ **Matplotlib & Plotly** for visualization (static + interactive)

---

## 🩺 Why This Matters

TB remains a global health challenge. Chest X-rays are cheap and widely available, but hard to interpret — especially for early learners or in low-resource settings.

By simulating **3D depth perception** from a standard 2D image, this tool helps:
- Visualize the **extent and shape** of TB patches
- Create more **intuitive, engaging visuals**
- Assist in **training, diagnosis, and presentations**

---

## 📁 Files in This Repo

| File | Description |
|------|-------------|
| `Assignment_TB.ipynb` | Full notebook: X-ray processing, TB labeling, depth estimation, 3D visualization |
| `README.md` | You're here! Project summary and instructions |

---

## 🧠 How It Works

### 🖼️ 1. Load a TB-positive chest X-ray  
We use sample X-rays from publicly available datasets like Montgomery or Shenzhen (or your own image).

### 📦 2. Annotate the TB Region  
We highlight the infected area with a bounding box + label (`"Active Tuberculosis"`), using OpenCV.

### 🧠 3. Estimate Depth Using MiDaS  
MiDaS is a deep learning model that guesses depth from a single image. It returns a **depth map** representing the "3D feel" of the X-ray.

### 🌐 4. Visualize in 3D  
We use:
- `Matplotlib` for a side-by-side depth map view
- `Plotly` for an **interactive 3D surface** — zoom, rotate, and explore

---

## 📸 Demo Preview

| 2D X-ray (with TB label) | MiDaS Depth Map | 3D Surface View |
|--------------------------|-----------------|-----------------|
| ![](./images/original_xray.png) | ![](./images/depth_map.png) | ![](./images/3d_view.gif) |

---

## 🚀 How to Run It (Colab Recommended)

1. Clone this repo or open the notebook in Google Colab.
2. Upload your own TB X-ray image (or use the one included).
3. Run all cells — you'll see:
   - The original labeled image
   - Estimated depth map
   - Interactive 3D surface

---

## 🧰 Tools Used

| Library | Purpose |
|--------|---------|
| `OpenCV` | Load + annotate images |
| `MiDaS` (via PyTorch Hub) | Single-image depth estimation |
| `Matplotlib` | Static plots |
| `Plotly` | Interactive 3D surface visualization |

---

## 📚 References

- [MiDaS by Intel ISL](https://github.com/intel-isl/MiDaS)
- [NIH Montgomery TB Dataset](https://lhncbc.nlm.nih.gov/publication/pub9931)
- [Shenzhen TB Dataset](https://lhncbc.nlm.nih.gov/publication/pub9931)

---

## 💡 Future Ideas

- Add real segmentation masks (not just bounding boxes)
- Animate 360° rotation of the X-ray
- Try with other medical images (e.g., pneumonia, COVID-19)
- Improve labeling using AI object detection

---

## 🙌 Acknowledgements

Big thanks to open-source heroes — Intel ISL, NIH, and all contributors to medical AI.

---

## 📬 Contact

Have ideas or feedback?  
Open an issue or reach me on [GitHub](https://github.com/yourusername)!

---

