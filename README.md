# Semantic-Text-Retrieval-using-Sentence-Embeddings
# 🔎 Semantic Text Retrieval using Sentence Embeddings

## 📌 Project Overview

This project implements a **semantic text retrieval system** that returns the top-k most semantically similar sentences for a given query.

Unlike keyword-based search, this system understands **meaning** using sentence embeddings and cosine similarity.

---

## 🎯 Problem Statement

Given:
- A dataset of short sentences (FAQs, product descriptions, etc.)

Task:
- Convert sentences into vector embeddings
- Compute cosine similarity between a query and dataset
- Retrieve the top-k most semantically similar sentences

Evaluation:
- Manual relevance check on 20 queries
- Precision@5 metric (optional)

---

## 🧠 Methodology

### 1️⃣ Sentence Embeddings
We use **SBERT (Sentence-BERT)** via the `sentence-transformers` library.

Model used:
- `all-MiniLM-L6-v2`

This model generates 384-dimensional contextual sentence embeddings optimized for semantic similarity tasks.

### 2️⃣ Similarity Computation
Cosine similarity is computed between:
- Query embedding
- Dataset embeddings

### 3️⃣ Top-k Retrieval
Sentences are ranked by similarity score, and the top-k most similar sentences are returned.

---

## 📊 Example Output

| Query | Rank | Retrieved Sentence | Similarity Score |
|-------|------|-------------------|------------------|
| I forgot my password | 1 | How can I reset my password? | 0.89 |
| I forgot my password | 2 | Steps to change login credentials | 0.86 |

---

## 📈 Evaluation

We performed:
- Manual relevance evaluation on 20 queries
- Computed Precision@5

### Precision@5 Formula:

Precision@5 = (Number of relevant results in top 5) / 5

---

## ⚠ Error Analysis

Observed error types:

- Synonym mismatch (e.g., "purchase" vs "buy")
- Topic similarity but different intent
- Keyword bias
- Short query ambiguity

---

## 🛠 Technologies Used

- Python
- Sentence-Transformers
- Scikit-learn
- NumPy
- Pandas

---

## 🚀 How to Run

### 1️⃣ Clone Repository
```bash
git clone https://github.com/your-username/semantic-text-retrieval.git
cd semantic-text-retrieval
