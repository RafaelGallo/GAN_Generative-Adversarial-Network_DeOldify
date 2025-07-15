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

<img width="982" height="691" alt="image" src="https://github.com/user-attachments/assets/435b6cd5-2066-42a6-a54f-5e5b56206239" />
<img width="957" height="691" alt="image" src="https://github.com/user-attachments/assets/da7f723c-e824-4676-a41c-4d58fb0bc2ee" />
<img width="927" height="691" alt="image" src="https://github.com/user-attachments/assets/ba33f64f-fe3d-425d-9d14-64fcc96033da" />
<img width="989" height="532" alt="image" src="https://github.com/user-attachments/assets/80d63d0b-1d1d-42d4-87b1-7f8c7dc866cd" />
<img width="989" height="500" alt="image" src="https://github.com/user-attachments/assets/32850cc7-f9a1-42ae-b474-7f73f4d9fc3c" />
<img width="989" height="502" alt="image" src="https://github.com/user-attachments/assets/d6f60a4b-166f-44c1-9377-278262d0aad1" />
<img width="989" height="502" alt="image" src="https://github.com/user-attachments/assets/38ec7fbb-04cd-45f6-b642-8c2a48121a7a" />
<img width="918" height="691" alt="image" src="https://github.com/user-attachments/assets/7b926860-fad4-4bcc-9c6b-e95cbeabb020" />
<img width="989" height="502" alt="image" src="https://github.com/user-attachments/assets/d2d46e45-ce34-4b78-abee-8fa46c247ce2" />

## 🖼️ Image Credits (APA Style)

The original black-and-white images used in this project were sourced from public and educational websites for research and demonstrative purposes only. Below are the citations in APA format:

1. Folha de S.Paulo. (2020, October). *Quem foi Tarsila do Amaral?* \[Web story]. Retrieved July 15, 2025, from [https://www1.folha.uol.com.br/webstories/cultura/2020/10/quem-foi-tarsila-do-amaral/](https://www1.folha.uol.com.br/webstories/cultura/2020/10/quem-foi-tarsila-do-amaral/)

2. Século XX Wiki. (n.d.). *Pedro II do Brasil*. Fandom. Retrieved July 15, 2025, from
[https://seculo-xx.fandom.com/pt-br/wiki/Pedro\_II\_do\_Brasil](https://seculo-xx.fandom.com/pt-br/wiki/Pedro_II_do_Brasil)

4. UOL Universa. (2019, April 6). *Por que Tarsila do Amaral foi uma mulher à frente do seu tempo?* Retrieved July 15, 2025, from [https://www.uol.com.br/universa/noticias/redacao/2019/04/06/por-que-tarsila-do-amaral-foi-uma-mulher-a-frente-do-seu-tempo.htm](https://www.uol.com.br/universa/noticias/redacao/2019/04/06/por-que-tarsila-do-amaral-foi-uma-mulher-a-frente-do-seu-tempo.htm)

5. BOL UOL. (2016, January 23). *São Paulo em 100 imagens do passado* (Photo 1). Retrieved July 15, 2025, from [https://www.bol.uol.com.br/listas/2016/01/23/sao-paulo-em-100-imagens-do-passado.htm?mode=list\&foto=1](https://www.bol.uol.com.br/listas/2016/01/23/sao-paulo-em-100-imagens-do-passado.htm?mode=list&foto=1)

> All rights belong to the original authors and publishers. The use of these images in this project is strictly non-commercial and educational.

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

**Rafael Gallo - Data Scientist**

📍 Brazil 

🌐 [LinkedIn](https://www.linkedin.com/in/rafael-g-986a73150/) 

📂 [GitHub](https://github.com/RafaelGallo)

## 📄 License
This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

