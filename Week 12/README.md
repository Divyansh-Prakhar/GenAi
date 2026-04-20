# 🤖 Generative Chatbot with Attention (LSTM + Attention)

## 📌 Overview

This project implements a **text generation chatbot using an LSTM-based Seq2Seq model with Attention**.

The goal is to demonstrate how **attention mechanisms improve contextual understanding** by allowing the model to focus on important words in the input sentence while generating responses.

---

## 🎯 Objective

- Build a chatbot that generates responses from user input  
- Use **Attention mechanism** to improve response quality  
- Understand how deep learning models handle **sequence-to-sequence tasks**

---

## 🧠 Key Concept: Attention Mechanism

Traditional Seq2Seq models encode the entire input into a fixed vector.

➡️ Attention improves this by:

- Assigning **weights to each input word**  
- Focusing more on **relevant words**  
- Improving long sentence understanding  

### Example
Input: "how are you"
Output: "i am fine"


👉 The model focuses more on the word **"you"**

---

## ⚙️ Model Architecture
Input Sentence
↓
Embedding Layer
↓
LSTM Encoder
↓
Attention Layer
↓
LSTM Decoder
↓
Fully Connected Layer
↓
Generated Output


---

## 📂 Dataset

### For Demonstration:
- Small custom dataset of conversation pairs  

### For Real-World Usage:
- Cornell Movie Dialog Dataset (recommended)

---

## 🏋️ Training Details

- **Loss Function:** CrossEntropyLoss  
- **Optimizer:** Adam  
- **Epochs:** 200  
- **Framework:** PyTorch  

---

## 📊 Results

### Training Loss
Epoch 0 → Loss: 2.8992
Epoch 50 → Loss: 0.0195
Epoch 100 → Loss: 0.0065
Epoch 150 → Loss: 0.0034


### Model Outputs
Input: hello → hi how are you
Input: how are you → i am fine


---

## ⚠️ Limitations

- Small dataset → model **overfits (memorizes)**  
- Not suitable for real-world conversations  
- Limited vocabulary  

---

## 🚀 Future Improvements

- Train on **Cornell Movie Dialog Dataset**  
- Add **beam search decoding**  
- Visualize **attention weights**  
- Deploy as a **web chatbot (Streamlit / FastAPI)**  
- Improve generalization with larger datasets  

---

## 🛠️ How to Run

1. Open Google Colab or Jupyter Notebook  
2. Run the provided code  
3. Train the model  
4. Test using:

python
print(generate("hello"))
print(generate("how are you"))

📚 Technologies Used
Python
PyTorch
LSTM (RNN)
Attention Mechanism
🙌 Conclusion

This project demonstrates how Attention enhances sequence models by enabling the model to dynamically focus on relevant input tokens, leading to better text generation.

📎 Author

Pratik Sinha

