# CSET419 – Introduction to Generative AI  
## Lab – 5  
### Baseline CNN for Image-to-Image Translation (Encoder–Decoder without GAN)

---

## 🎯 Objective

To implement a baseline Encoder–Decoder Convolutional Neural Network (CNN) for paired image-to-image translation and analyze its performance using reconstruction loss.

---

## 📌 Experiment Tasks

1. Load paired images (CIFAR10 dataset)  
2. Normalize images to range [-1, 1]  
3. Train an Encoder–Decoder CNN  
4. Compute reconstruction loss (MSE / L1)  
5. Visualize translated (reconstructed) images  

---

## 📂 Dataset

**CIFAR10 Dataset**

- 60,000 RGB images  
- Image size: 32 × 32  
- 10 object classes  
- Used in paired setting (Input = Target image)

---

## 🧠 Model Architecture

### Encoder
- Conv2D (3 → 64), ReLU  
- Conv2D (64 → 128), ReLU  

### Decoder
- ConvTranspose2D (128 → 64), ReLU  
- ConvTranspose2D (64 → 3), Tanh  

The final activation is **Tanh** to ensure output is in range [-1, 1].

---

## 📉 Loss Function

Reconstruction Loss:

- Mean Squared Error (MSE)  
or  
- L1 Loss  

The model minimizes the difference between the input image and reconstructed image.

---

## ⚙️ Training Configuration

- Optimizer: Adam  
- Learning Rate: 0.001  
- Epochs: 5  
- Batch Size: 16  
- Device: CPU / GPU  

---

## 📊 Results & Observation

- The reconstructed images appear slightly blurry.
- Pixel-wise reconstruction losses (MSE/L1) cause smoothing.
- No adversarial training is used.

---

## ✅ Conclusion

The baseline Encoder–Decoder CNN successfully reconstructs CIFAR10 images.  
However, outputs are blurry due to pixel-wise loss limitations.

To improve results:
- Use U-Net (skip connections)
- Use GAN-based training
- Use perceptual loss
