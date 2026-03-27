# 🎨 Neural Style Transfer (Lab 7)

## 📌 Overview

This project implements **Neural Style Transfer** using a pretrained **VGG19 model** in PyTorch.
It combines:

* **Content Image** → structure
* **Style Image** → artistic texture

👉 Output: A new image that preserves content but adopts the style.

---

## 🎯 Objective

To understand and implement style transfer using deep learning by:

* Extracting features from CNN
* Computing style using Gram matrices
* Optimizing an image using backpropagation

---

## 🧠 Key Concepts

* Convolutional Neural Networks (CNN)
* Feature extraction using VGG19
* Content Loss (structure preservation)
* Style Loss (texture representation)
* Gram Matrix (captures style)
* Image optimization using gradient descent

---

## ⚙️ Tech Stack

* Python
* PyTorch
* Torchvision
* PIL (Python Imaging Library)
* Matplotlib

---

## 📂 Workflow

### 1. Load Images

* Content image
* Style image

### 2. Preprocess

* Resize to 256×256
* Convert to tensor

### 3. Load Model

* Pretrained VGG19
* Freeze all layers

### 4. Feature Extraction

* Extract content features (deep layer)
* Extract style features (multiple layers)

### 5. Compute Gram Matrix

* Represents style (texture patterns)

### 6. Initialize Generated Image

* Clone content image
* Enable gradient updates

### 7. Define Loss

* Content Loss = difference in features
* Style Loss = difference in Gram matrices
* Total Loss = Content + (Style × weight)

### 8. Optimization

* Use Adam optimizer
* Update image pixels iteratively

### 9. Output

* Display final stylized image

---

## 📊 Results

* Loss decreases over iterations
* Final image shows:

  * Content preserved
  * Style applied successfully

---

## 🧾 Sample Output

Stylized image generated after optimization.

---

## ❓ Viva Questions

1. Why use VGG19?
2. What is a Gram Matrix?
3. Why freeze model weights?
4. Why use multiple layers for style?
5. Why is style loss weighted higher?

---

## ⚡ Key Takeaways

* Style = correlations between features
* Content = actual feature representation
* Optimization modifies image pixels, not model weights

---

## 🚀 How to Run

```bash
pip install torch torchvision matplotlib pillow
python style_transfer.py
```

---

## 🧠 Summary

Neural Style Transfer uses deep neural networks to blend the **content of one image** with the **style of another**, producing visually artistic results.

---

✨ *Content = Structure | Style = Texture | Output = Blend of both*
