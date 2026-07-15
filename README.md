# 🖼️ AI HD Image Enhancer — Real-ESRGAN x4plus



https://github.com/user-attachments/assets/f861ed98-db8d-445f-8228-2bfa004e5249


<img width="1600" height="855" alt="WhatsApp Image 2026-06-30 at 7 01 46 PM (2)" src="https://github.com/user-attachments/assets/c4257991-c3d0-4bd1-90a9-2e3c17579e11" />

<img width="1359" height="764" alt="Screenshot 2026-07-15 114215" src="https://github.com/user-attachments/assets/76e9a704-c596-4a2d-95ae-787600b3939d" />






<div align="center">

![Real-ESRGAN](https://img.shields.io/badge/Model-Real--ESRGAN%20x4plus-blue?style=for-the-badge&logo=pytorch)
![Python](https://img.shields.io/badge/Python-3.9%2B-green?style=for-the-badge&logo=python)
![HuggingFace](https://img.shields.io/badge/🤗%20Deployed-HuggingFace%20Spaces-yellow?style=for-the-badge)
![Google Colab](https://img.shields.io/badge/Notebook-Google%20Colab-orange?style=for-the-badge&logo=googlecolab)
![License](https://img.shields.io/badge/License-MIT-red?style=for-the-badge)

**Transform any blurry, low-resolution photo into stunning 4× HD quality using the official pretrained Real-ESRGAN x4plus model — no training required.**

[🚀 **Try Live Demo**](https://huggingface.co/spaces/Maliktg5/AI_HD_Image_Enhancer_Real-ESRGAN_x4plus) · [📓 Open in Colab](#-google-colab-notebook) · [📌 Report Bug](https://github.com/mudassar2224/AI-HD-Image-Enhancer-Real-ESRGAN_x4plus/issues)

</div>

---

## 📸 Demo — Before & After

> Upload any image → Get 4× HD quality output in seconds.

| Original (Low-Res) | Enhanced (4× HD) |
|---|---|
| 720 × 480 px | 2880 × 1920 px |
| Blurry / compressed | Sharp, detailed, restored |

*Live interactive slider comparison available in the [Hugging Face Space](https://huggingface.co/spaces/Maliktg5/AI_HD_Image_Enhancer_Real-ESRGAN_x4plus)*

---

## ✨ Features

- 🔍 **4× Super Resolution** — upscales any image from low-res to HD using Real-ESRGAN x4plus
- 🖥️ **GPU / CPU support** — runs on CUDA GPU (fast) or CPU (no GPU needed)
- 🖼️ **All image formats** — JPG, JPEG, PNG, BMP, WEBP, and more
- 🔄 **Interactive comparison slider** — drag to compare original vs enhanced side-by-side
- 📥 **One-click download** — download your enhanced PNG directly from the browser
- 🌐 **Live web app** — deployed on Hugging Face Spaces, accessible from any device
- 📓 **Colab notebook** — full 19-section notebook, beginner-friendly, runs top to bottom
- 📊 **Quality metrics** — PSNR and SSIM scores computed automatically
- ⚡ **No training** — uses official pretrained weights only (inference only)

---

## 🚀 Quick Start — Try Online (No Setup)

**👉 [Open the Live Demo on Hugging Face Spaces](https://huggingface.co/spaces/Maliktg5/AI_HD_Image_Enhancer_Real-ESRGAN_x4plus)**

1. Click the link above
2. Upload any image (drag & drop or click to browse)
3. Click **Enhance Image (×4)**
4. Drag the comparison slider to see the difference
5. Click **Download Enhanced Image**

No installation. No account. Works on mobile and desktop.

---

## 📓 Google Colab Notebook

Run the full pipeline in Google Colab — no local setup required.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/mudassar2224/AI-HD-Image-Enhancer-Real-ESRGAN_x4plus)

**The notebook covers 19 sections:**

| # | Section |
|---|---|
| 1 | Project Introduction (Super Resolution, Real-ESRGAN explained) |
| 2 | GPU / CUDA / PyTorch environment check |
| 3 | Install all dependencies automatically |
| 4 | Clone official Real-ESRGAN GitHub repository |
| 5 | Download pretrained RealESRGAN_x4plus weights |
| 6 | Import all libraries |
| 7 | Configuration & folder setup |
| 8 | Upload image via Colab widget |
| 9 | Load model with `load_model()` function |
| 10 | Enhancement with `enhance_image()` function |
| 11 | Run inference with progress messages |
| 12 | Side-by-side before/after comparison |
| 13 | Download enhanced image |
| 14 | Performance report (time, GPU memory) |
| 15 | Error handling utilities |
| 16 | Centralized configuration block |
| 17 | Clean OOP wrapper class |
| 18 | PSNR & SSIM quality metrics (Bonus) |
| 19 | Final summary & next steps |
---

## ⚙️ How It Works

```
Input Image (any resolution)
        │
        ▼
  Pre-processing
  (resize if needed, BGR conversion)
        │
        ▼
  RRDBNet Architecture
  (23 RRDB blocks, 64 feature channels)
        │
        ▼
  RealESRGANer Inference
  (official pretrained weights)
        │
        ▼
  4× Upscaled Output
  (sharpened, denoised, restored)
        │
        ▼
  Download / Compare
```

**Model Architecture:** RRDBNet (Residual-in-Residual Dense Block Network)  
**Weights:** Official `RealESRGAN_x4plus.pth` (~67 MB) from [xinntao/Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)  
**Upscale factor:** 4× (e.g. 720×480 → 2880×1920)

---

## 🛠️ Local Installation

### Prerequisites
- Python 3.9+
- CUDA GPU (optional but recommended for speed)

### Steps

```bash
# 1. Clone this repository
git clone https://github.com/mudassar2224/AI-HD-Image-Enhancer-Real-ESRGAN_x4plus.git
cd AI-HD-Image-Enhancer-Real-ESRGAN_x4plus

# 2. Clone the official Real-ESRGAN repo
git clone https://github.com/xinntao/Real-ESRGAN.git
cd Real-ESRGAN && pip install -e . && cd ..

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download pretrained weights
mkdir -p weights
wget -O weights/RealESRGAN_x4plus.pth \
  https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.0/RealESRGAN_x4plus.pth

# 5. Run the Gradio app locally
python app.py
```

Then open `http://localhost:7860` in your browser.

---

## 📦 Dependencies

```
torch
torchvision
opencv-python-headless
numpy
Pillow
basicsr
facexlib
gfpgan
realesrgan
gradio>=4.0.0
scikit-image
```

---

## 📊 Performance

| Metric | Value |
|---|---|
| Upscale Factor | 4× |
| Typical Enhancement Time (GPU T4) | ~3–8 seconds |
| Typical Enhancement Time (CPU) | ~60–180 seconds |
| Max Input Size (auto-resize) | 1500px on longest side |
| Output Format | PNG (lossless) |
| PSNR (vs downscaled enhanced) | ~35–42 dB (image-dependent) |
| SSIM | ~0.90–0.98 |

---

## 🧠 About Real-ESRGAN

Real-ESRGAN is a state-of-the-art image restoration model developed by [Xintao Wang et al.](https://arxiv.org/abs/2107.10833). Unlike traditional upscaling methods (bicubic, lanczos), Real-ESRGAN uses a deep neural network trained on real-world degraded images to:

- Recover fine texture and detail
- Remove JPEG compression artifacts
- Denoise and sharpen blurry photos
- Reconstruct facial features and natural textures

**Paper:** [Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data](https://arxiv.org/abs/2107.10833) (ICCV 2021)

---

## 🌐 Deployment

This project is deployed as a **Gradio web application** on **Hugging Face Spaces**.

| Platform | Link |
|---|---|
| 🤗 Hugging Face Spaces | [Maliktg5/AI_HD_Image_Enhancer_Real-ESRGAN_x4plus](https://huggingface.co/spaces/Maliktg5/AI_HD_Image_Enhancer_Real-ESRGAN_x4plus) |
| 📦 GitHub Repository | [mudassar2224/AI-HD-Image-Enhancer-Real-ESRGAN_x4plus](https://github.com/mudassar2224/AI-HD-Image-Enhancer-Real-ESRGAN_x4plus) |

Deployment was automated directly from **Google Colab** using the `huggingface_hub` Python API — no manual file upload to GitHub required.

---

## 🤝 Credits

- **Real-ESRGAN** by [Xintao Wang](https://github.com/xinntao/Real-ESRGAN) — the core model and official inference pipeline
- **BasicSR** — the backbone training and inference framework
- **Gradio** — the web UI framework
- **Hugging Face Spaces** — hosting and deployment

---

## 📄 License

This project is licensed under the **MIT License**.  
The Real-ESRGAN model weights are subject to the [Real-ESRGAN license](https://github.com/xinntao/Real-ESRGAN/blob/master/LICENSE).

---

## 👤 Author

**Muhammad Mudassar**  
B.S. Artificial Intelligence — University of Management and Technology (UMT)

[![GitHub](https://img.shields.io/badge/GitHub-mudassar2224-black?style=flat&logo=github)](https://github.com/mudassar2224)
[![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-Maliktg5-yellow?style=flat)](https://huggingface.co/Maliktg5)

---

<div align="center">

⭐ **If this project helped you, please give it a star!** ⭐

</div>
