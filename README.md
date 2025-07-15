# 🧠 DeOldify GAN — Image Colorization with Generative Adversarial Networks

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![Model](https://img.shields.io/badge/Model-DeOldify-brightgreen)](https://github.com/jantic/DeOldify)
[![Type](https://img.shields.io/badge/Type-Image%20Colorization-orange)]()
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Framework](https://img.shields.io/badge/Framework-FastAI%20%2B%20PyTorch-lightgrey)
![Model](https://img.shields.io/badge/Model-DeOldify-brightgreen)
![Type](https://img.shields.io/badge/Task-Image%20Colorization-orange)
![Status](https://img.shields.io/badge/Status-Complete-success)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Colab](https://img.shields.io/badge/Run%20on-Google%20Colab-blueviolet?logo=googlecolab)
![PyTorch](https://img.shields.io/badge/PyTorch-1.12%2B-EE4C2C?logo=pytorch)
![FastAI](https://img.shields.io/badge/FastAI-2.7%2B-lightgrey?logo=fastai)
![Model](https://img.shields.io/badge/Model-DeOldify-brightgreen)
![Task](https://img.shields.io/badge/Task-Image%20Colorization-orange)
![Architecture](https://img.shields.io/badge/Architecture-GAN%20%2B%20U--Net-blueviolet)
![GPU Support](https://img.shields.io/badge/GPU-Compatible-green?logo=nvidia)
![Colab](https://img.shields.io/badge/Run%20on-Google%20Colab-blueviolet?logo=googlecolab)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter)
![Input](https://img.shields.io/badge/Input-Grayscale%20Images-black)
![Output](https://img.shields.io/badge/Output-Colorized%20Photos-green)
![Last Commit](https://img.shields.io/github/last-commit/RafaelGallo/GAN_Generative-Adversarial-Network_DeOldify)
![Repo Size](https://img.shields.io/github/repo-size/RafaelGallo/GAN_Generative-Adversarial-Network_DeOldify)
![Stars](https://img.shields.io/github/stars/RafaelGallo/GAN_Generative-Adversarial-Network_DeOldify?style=social)

# ![DeOldify Logo](https://github.com/RafaelGallo/GAN_Generative-Adversarial-Network_DeOldify/blob/main/img/log.png?raw=true)

## 📌 Project Overview

This project applies the **DeOldify** architecture — a state-of-the-art model based on **Generative Adversarial Networks (GANs)** — to automatically colorize black-and-white photographs, recovering visual details and bringing old memories back to life.

## 🎯 Objectives

* Transform grayscale images into realistic colorized versions.
* Utilize perceptual, adversarial, and pixel-level learning for high-fidelity results.
* Enable inference on both local images and external URLs.

## 🧠 Model Architecture

The colorization model is composed of:

* **Generator:** A **U-Net** architecture with a **ResNet34** or **ResNet101** encoder pretrained on ImageNet.
* **Discriminator:** PatchGAN-style CNN to differentiate real vs generated colors.
* **Losses:**

  * Perceptual loss (based on VGG features)
  * Adversarial loss (via GAN training)
  * Pixel-wise L1/L2 loss
* **Enhancements:** Adjustable `render_factor` to control resolution and detail.

## 🗂️ Project Structure

```
DeOldify-GAN/
├── img/                      # Visual assets (logo, examples)
├── input/                    # Input grayscale images
├── output/                   # Colorized output images
├── models/                   # Pretrained models
├── deoldify/                 # DeOldify source code
├── run_colorizer.py          # Main script for inference
├── README.md
└── requirements.txt
```

## 💡 How It Works

1. Load the pre-trained DeOldify model.
2. Feed a grayscale image or URL.
3. The generator predicts a colorized version.
4. The discriminator refines realism through adversarial training.
5. Output is saved and optionally compared side-by-side.

## 🚀 Getting Started

### ✅ Prerequisites

* Python 3.8 or 3.9
* PyTorch
* FastAI
* Jupyter or Google Colab (recommended for GPU support)

### 📦 Installation

```bash
git clone https://github.com/RafaelGallo/GAN_Generative-Adversarial-Network_DeOldify.git
cd GAN_Generative-Adversarial-Network_DeOldify
pip install -r requirements.txt
```

## 🖼️ Example Results

### Before and After

| Colorized (DeOldify)   |
| ---------------------- | 
|<img width="482" height="638" alt="image" src="https://github.com/user-attachments/assets/4c26ccc0-3c53-406d-9962-3756740c3f77" />|
|<img width="640" height="348" alt="image" src="https://github.com/user-attachments/assets/f58f7fc7-bbee-4800-a83c-63749a96d0c6" />|
|<img width="640" height="348" alt="image" src="https://github.com/user-attachments/assets/4481962d-41da-4e1c-9cff-e826ae79230c" />|
|<img width="640" height="348" alt="image" src="https://github.com/user-attachments/assets/f462bd44-c392-48f3-aa3c-7f97b6361aba" />|
|<img width="430" height="636" alt="image" src="https://github.com/user-attachments/assets/c3380863-9879-4d99-8cd4-36f082f9a491" />|
|<img width="640" height="348" alt="image" src="https://github.com/user-attachments/assets/a690c839-5121-47ba-ba1c-c77e526bc696" />|
|<img width="640" height="348" alt="image" src="https://github.com/user-attachments/assets/321b4d7d-3d62-405a-936d-136742596da0" />|
|<img width="436" height="644" alt="image" src="https://github.com/user-attachments/assets/6224b73f-37a4-4c53-b095-491ec34b1909" />|
|<img width="640" height="425" alt="image" src="https://github.com/user-attachments/assets/676caa0d-9099-40cc-af76-8b5c7da65e06" />|



## 🧪 Inference

### 🔗 From an Image URL (Colab)

```python
colorizer.plot_transformed_image_from_url(
    url="https://example.com/black-and-white-photo.jpg",
    render_factor=35,
    compare=True
)
```

### 📁 From a Local File

```python
colorizer.plot_transformed_image(
    'input/photo_bw.jpg',
    render_factor=30,
    results_dir=Path('./output'),
    compare=True
)
```

## 📊 Evaluation Metrics

| Metric            | Description                              |
| ----------------- | ---------------------------------------- |
| PSNR              | Peak Signal-to-Noise Ratio               |
| SSIM              | Structural Similarity Index              |
| Inception Score   | Image quality from classification logits |
| Visual inspection | Manual qualitative evaluation            |

## 📚 References

* [DeOldify Original Repo](https://github.com/jantic/DeOldify)
* [Paper: Generative Adversarial Networks (Goodfellow et al., 2014)](https://arxiv.org/abs/1406.2661)
* [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597)
* [FastAI Documentation](https://docs.fast.ai)

## 👨‍💻 Author

**Rafael Gallo**
Data Scientist | Deep Learning Researcher
📍 Brazil | 🌐 [LinkedIn](https://www.linkedin.com/in/rafaelgallo/) | 📂 [GitHub](https://github.com/RafaelGallo)

## 📄 License
This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

