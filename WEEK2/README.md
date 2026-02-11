# CSET419 – Introduction to Generative AI  
## Lab 2: Training a Basic GAN for Image Generation

### Objective
The objective of this experiment is to implement and train a basic Generative Adversarial Network (GAN) to generate synthetic images similar to a real dataset (MNIST/Fashion-MNIST). The generated images are evaluated over training epochs and further analyzed using a pre-trained classifier.

---

### Dataset Used
- Dataset: MNIST (Handwritten Digits)
- Image Size: 28 × 28 grayscale
- Source: TensorFlow Keras Dataset

---

### Input Parameters
The following parameters were used during training:

- Dataset Choice: `mnist`
- Epochs: `30`
- Batch Size: `128`
- Noise Dimension: `100`
- Learning Rate: `0.0002`
- Save Interval: `5 epochs`

---

### Model Architecture

#### Generator
- Input: Random noise vector
- Layers: Dense + LeakyReLU
- Output: 28×28 grayscale image
- Activation: Sigmoid

#### Discriminator
- Input: Image
- Layers: Dense + LeakyReLU
- Output: Probability (Real/Fake)
- Activation: Sigmoid

---

### Training Procedure
- The Discriminator is trained on both real and generated (fake) images.
- The Generator is trained to fool the Discriminator.
- Training is performed for the given number of epochs with alternating optimization.
- Losses for both Generator and Discriminator are computed and logged.

---

### Generated Outputs

#### Output 1: Training Logs
Epoch-wise logs displaying:

#### Output 2: Generated Samples
- Folder: `generated_samples/`
- Images saved every 5 epochs
- Each image contains a 5×5 grid (25 samples)

#### Output 3: Final Generated Images
- Folder: `final_generated_images/`
- Total Images Generated: 100

#### Output 4: Label Prediction
- A pre-trained classifier was used to predict labels of generated images.
- Label distribution was printed to analyze diversity.

---

### Tools & Libraries Used
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Google Colab

---

### Conclusion
The GAN was successfully trained to generate synthetic images resembling the MNIST dataset. The generated images improved in quality over epochs, and the label prediction results confirmed that the GAN learned meaningful patterns from the dataset.

---

### Submitted By
**Name:** Divyansh Prakhar  
**Course:** CSET419 – Introduction to Generative AI  
**Lab:** 2

