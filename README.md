# 🧠 Multi-Label Text Classification using Word2Vec, GloVe, FastText & BERT (PyTorch)

This repository implements a complete end-to-end pipeline for **multi-label text classification** using four different embedding models:

- **Word2Vec**
- **GloVe**
- **FastText**
- **BERT (Sentence-Transformers)**

The project uses the *Consumer Review of Clothing Product* dataset from Kaggle and compares how modern contextual embeddings outperform traditional static embeddings in real-world text classification tasks.

---

## 📌 Key Features

✔ Multi-label classification  
✔ Four embedding models compared under identical architecture  
✔ Clean preprocessing pipeline  
✔ Deep neural network classifier using PyTorch  
✔ Automatically saved results (CSV + charts)  
✔ Embedding caching for fast re-runs  
✔ Fully reproducible single-script pipeline  

---

## 📂 Dataset Information

**Dataset Name:** Consumer Review of Clothing Product  
**Source:** Kaggle  
**Link:** https://www.kaggle.com/datasets/jocelyndumlao/consumer-review-of-clothing-product


---

## 🧩 Embedding Models Used
🔹 Word2Vec

Trained on review corpus (300D)

🔹 GloVe

Pretrained vectors (100D / 300D)

🔹 FastText

Subword-level embeddings

Trained on corpus or loaded externally

🔹 BERT (Sentence-Transformers)

Model used: all-MiniLM-L6-v2

Produces contextual embeddings (384D)

Expected to outperform static embeddings

------
# 📥 Preprocessing

Text preprocessing includes:

Lowercasing

Tokenization using NLTK

Removing special characters

Handling missing values

Converting text to embeddings

Multi-label targets are generated using:

Recommended Indicator (binary)

Department Name

Class Name

Fallback labels are used if any columns are missing.


-------
## 🚀 Pipeline Overview

### **1. Load and clean dataset**
- Lowercase text  
- Remove punctuation  
- Tokenize  
- Handle missing values  

### **2. Build multi-label targets**
- Convert `Recommended IND`
- One-hot encode `Department Name`
- One-hot encode `Class Name`
- If missing → fallback `Cloth_class` + `Cons_rating`

### **3. Generate embeddings**
- **Word2Vec:** trained on corpus  
- **GloVe:** pretrained (optional download)  
- **FastText:** trained on corpus, handles OOV  
- **BERT-SBERT:** contextual semantic vectors  

### **4. Train PyTorch classifier**
A 2-layer neural network:
Loss = `BCEWithLogitsLoss`  
Optimizer = `Adam`  

### **5. Evaluate using**
- Micro F1  
- Macro F1  
- Precision  
- Recall  
- AUC per label  

### **6. Export results**

Saved to: csv file

----------------
# 📈 Expected Results

| Embedding Model  | Expected Performance  |
| ---------------- | --------------------- |
| **BERT (SBERT)** | ⭐ Highest performance |
| FastText         | Very strong           |
| Word2Vec         | Good baseline         |
| GloVe            | Solid older method    |

-----------
# 📌 Key Insights

Contextual models > Static averages

FastText excels in noisy real-world datasets

Domain-trained Word2Vec/FT improves significantly

Multi-label formulation is more realistic than sentiment-only models






