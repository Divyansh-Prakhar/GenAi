# WEEK 3 – Variational Autoencoder (VAE)
**Course:** CSET419 – Introduction to Generative AI  
**Lab:** Week 3  
**Student:** Divyansh Prakhar  
**Dataset:** MNIST  
**Framework:** PyTorch  

---

## 🎯 Objective
The objective of this lab is to understand and implement a **Variational Autoencoder (VAE)** in order to:
- Learn latent representations of image data
- Generate diverse and novel samples from a learned probability distribution
- Understand the role of encoder, decoder, latent space, and KL-divergence

---

## 📚 Theory Overview
A **Variational Autoencoder (VAE)** is a generative model that learns a **probability distribution** over the data instead of learning fixed latent vectors like a traditional autoencoder.

Unlike standard autoencoders:
- VAEs learn **mean (μ)** and **variance (σ²)** of the latent space
- Sampling is done using the **reparameterization trick**
- A **KL-divergence loss** regularizes the latent space to follow a normal distribution

---

## 🧪 Experiment Tasks Performed

### ✅ Task 1: Dataset Preparation
- Loaded the MNIST dataset
- Normalized input images
- Split data into training and testing sets

### ✅ Task 2: VAE Architecture
- Designed encoder network
- Computed latent mean (μ) and log variance (log σ²)
- Applied reparameterization trick
- Designed decoder network for image reconstruction

### ✅ Task 3: Loss Function
- Reconstruction loss using Binary Cross Entropy
- KL-divergence loss for latent space regularization
- Combined both losses into total VAE loss

### ✅ Task 4: Training
- Trained the VAE model for multiple epochs
- Observed gradual decrease in training loss
- Plotted training loss curve

### ✅ Task 5: Sample Generation
- Sampled random vectors from standard normal distribution
- Generated new digit images using the decoder

### ✅ Task 6: Latent Space Visualization (Optional)
- Reduced latent space to 2 dimensions
- Visualized latent representations using scatter plot

---

## 📊 Results and Observations
- Training loss decreases smoothly, indicating stable learning
- Reconstructed images are slightly blurred, which is expected in VAEs
- Generated samples resemble handwritten digits and are diverse
- Latent space shows meaningful clustering of digit classes

---

## 📁 Files Included
- `LAB3-GENAI.ipynb` – Complete VAE implementation
- `README.md` – Lab description and explanation

---

## ✅ Conclusion
The Variational Autoencoder was successfully implemented and trained on the MNIST dataset.  
The model learned meaningful latent representations and was able to generate new and diverse image samples, fulfilling all the objectives of the lab.

---

## 🔗 References
- Kingma & Welling, *Auto-Encoding Variational Bayes*
- PyTorch Documentation
- MNIST Dataset
