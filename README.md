# 🧠 Fine-Tuned Qwen2 7B VLM for LaTeX Equation Extraction from Images

This project presents a fine-tuned, 4-bit quantized version of **Qwen2-7B Vision-Language Model** capable of **accurately extracting LaTeX equations from images**. Using the **Unsloth optimization framework**, we enhanced the model's capability to interpret complex visual mathematical expressions with high precision and efficiency.

---

## 🔍 Overview

The project focuses on extracting LaTeX-formatted equations from mathematical images. We built upon the **Qwen2-7B VLM** and enhanced it through:
- **4-bit quantization** for memory efficiency.
- **Supervised Fine-Tuning (SFT)** using **LoRA adapters** and **PEFT (Parameter-Efficient Fine-Tuning)** techniques.
- **Custom dataset** of paired LaTeX equations and rendered images.
- **Full fine-tuning** of vision, language, attention, and MLP layers for comprehensive learning.

---

## 🛠️ Key Features

- 📦 **Quantized 4-bit model** optimized for efficient inference and reduced memory usage.
- 🔧 **LoRA + PEFT training** for scalable parameter updates with minimal compute.
- 📉 **Reduced training loss to 0.39** in just 30 optimization steps via strategic batch processing.
- 🧠 **Full-stack fine-tuning** (vision, language, attention, MLP).
- 📸 **High-precision LaTeX extraction** from real-world mathematical equation images.

---

## 🧪 Technical Details

- **Base Model**: [Qwen2-7B Vision-Language](https://huggingface.co/Qwen/Qwen-VL)
- **Optimization Framework**: [Unsloth](https://github.com/unslothai/unsloth)
- **Quantization**: 4-bit GPTQ for memory efficiency
- **Fine-Tuning Technique**: Supervised Fine-Tuning with LoRA adapters (via HuggingFace PEFT)
- **Dataset**: Custom-built LaTeX-image pairs dataset
- **Training Strategy**:
  - Full-layer fine-tuning (vision encoder, language decoder, attention, MLP)
  - 30 steps with batch-level optimization
  - Final loss: **0.39**

---

## 🖼️ Example Use Case

**Input Image**  
![equation_image](examples/sample_equation.png)

**Extracted LaTeX**
```latex
\int_{0}^{\infty} \frac{x^2}{e^x - 1} \, dx = \frac{\pi^4}{15}
