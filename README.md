# Neural Network Comparison for Text Generation  
## RNN vs LSTM vs Transformer (WikiText-2)

## Project Overview
This project implements and compares three neural network architectures for next-word prediction:

- Recurrent Neural Network (RNN)  
- Long Short-Term Memory (LSTM)  
- Transformer  

All models are trained and evaluated on the WikiText-2 dataset using the same preprocessing pipeline and training configuration to ensure a fair comparison.

---

## Objective
The goal of this project is to compare how different neural network architectures perform on a language modeling task.

Given a sequence of words, each model predicts the next word in the sequence.

---

## Models

### RNN
- Simple sequential model  
- Captures short-term dependencies  
- Suffers from vanishing gradient problem  

### LSTM
- Improved version of RNN  
- Handles long-term dependencies using gates  
- More stable than RNN  

### Transformer
- Uses self-attention mechanism  
- Processes sequences in parallel  
- Achieves best performance among the three  

---

## Dataset
- WikiText-2 dataset  
- Split into training, validation, and test sets  

---

## Pipeline

### 1. Data Preprocessing
- Tokenization  
- Vocabulary creation  
- Convert words to indices  
- Generate input-output sequences  

### 2. Dataset Preparation
- Fixed sequence length  
- Batch creation  
- Train / Validation / Test split  

### 3. Model Training
- Optimizer: Adam  
- Loss Function: Cross-Entropy Loss  
- Same batch size and sequence length for all models  

### 4. Evaluation
- Perplexity calculation  
- Loss tracking  

### 5. Text Generation
- Generate sample text from each model  
- Compare fluency and coherence  

---

## Evaluation Metrics

- Training Perplexity  
- Validation Perplexity  
- Test Perplexity  
- Number of Parameters  
- Training Time  
- Loss Curves  
- Generated Text Quality  

---

## Results Summary

| Model        | Strengths                     | Weaknesses                     |
|-------------|------------------------------|--------------------------------|
| RNN         | Simple and fast              | Poor long-term memory           |
| LSTM        | Better sequence learning     | Slower than RNN                 |
| Transformer | Best performance             | Computationally expensive       |

---

## Key Insights

- Transformer performs best overall  
- LSTM improves over RNN for longer sequences  
- RNN struggles with long dependencies  
- Attention mechanism improves performance significantly  

---

## Technologies Used

- Python  
- PyTorch / TensorFlow  
- NumPy  
- Matplotlib  

---

## How to Run

```bash
git clone <your-repo-link>
cd project-folder
pip install -r requirements.txt
python train.py
python evaluate.py
