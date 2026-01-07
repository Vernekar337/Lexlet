# lexlet

**lexlet** is a character-level neural name generator built using a simple **Multi-Layer Perceptron (MLP)**.  
The model learns patterns in names and generates new names one character at a time.

This project focuses on understanding the **foundational mechanics of language models** before scaling to larger architectures such as RNNs or Transformers.

---

## What this project does

- Trains a character-level language model on a dataset of names  
- Uses a fixed context window to predict the next character  
- Learns character embeddings  
- Applies an MLP to produce probability distributions over the vocabulary  
- Samples from the learned distribution to generate new names  

---

## Model Overview

- **Input:** Context window of previous characters  
- **Embedding layer:** Learns dense character representations  
- **Hidden layer:** Fully connected layer with non-linearity  
- **Output layer:** Produces logits over the character vocabulary  
- **Loss:** Cross-entropy loss  
- **Training:** Manual training loop (no high-level abstractions)

---

## Why lexlet?

Modern language models often feel like black boxes.  
**lexlet** is intentionally small and interpretable — built to understand:

- how text becomes tokens  
- how context is modeled numerically  
- how probability distributions over language are learned  
- why scaling (data, depth, attention) matters later  

---

## Sampling

After training, the model generates new names by:

1. Starting from a special start token  
2. Iteratively predicting the next character  
3. Sampling from the probability distribution  
4. Stopping when the end token is generated  

---

## Project Status

Completed as a foundational learning project.

Possible future extensions:
- N-gram model comparison  
- RNN-based sequence models  
- Transformer-based architectures  

---

## Acknowledgements

Inspired by educational implementations of character-level  
language modeling and neural network fundamentals.
