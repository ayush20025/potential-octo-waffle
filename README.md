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


