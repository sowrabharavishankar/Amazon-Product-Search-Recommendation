# Amazon Product Search & Recommendation System

A **content-based and semantic search** recommendation engine built using **TF-IDF** and **Sentence-BERT (SBERT)** embeddings.  
This project demonstrates how traditional keyword-based approaches compare with modern transformer-based models for retrieving semantically similar products from an Amazon-style dataset.

---

## Overview

This system allows users to:
- Input a **title** or **search query**
- Retrieve **top-N similar products**
- Compare **classical TF-IDF recommendations** vs **SBERT semantic recommendations**
- Visualize recommendation scores and product similarity

It combines product metadata such as **title**, **description**, and **category** to compute similarity scores that rank the most relevant items.

---

## Features

- 🧩 **TF-IDF + Cosine Similarity** for classical content-based filtering  
- 🧠 **SBERT embeddings** (`all-MiniLM-L6-v2`, `multi-qa-mpnet-base-dot-v1`) for semantic search  
- 🔍 Search by keyword or product title  
- 📊 Visualization of top recommendations using bar charts  
- 🗂️ Extendable for user-based or hybrid recommendation systems  

---

## Models Used

### 1. Content-Based Filtering (TF-IDF + Cosine Similarity)
Uses TF-IDF vectors to represent each product based on its **title**, **description**, and **category**.  
Similarity is computed using **cosine similarity**, returning items that share similar words.

✅ Pros:
- Simple and interpretable  
- Fast for small datasets  

❌ Cons:
- Cannot capture meaning or synonyms  
- Relies heavily on word overlap  

---

### 2. Semantic Search (Sentence-BERT)
Uses **Sentence-BERT embeddings** (`all-MiniLM-L6-v2` or `multi-qa-mpnet-base-dot-v1`) to capture **contextual meaning** of text.  
Embeddings are compared via cosine similarity to find semantically related products.

✅ Pros:
- Understands context and synonyms  
- Works even when keywords differ  
- High accuracy on descriptive text  

❌ Cons:
- Requires a pretrained model  
- Slightly heavier computationally  

---
TF-IDF Based Recommendation:

<img width="1105" height="296" alt="image" src="https://github.com/user-attachments/assets/d4c3cee6-8873-49bc-a86a-2eafe03eff96" />

SBERT Based Semantic Recommendation

<img width="1095" height="266" alt="image" src="https://github.com/user-attachments/assets/2703219b-87c0-41be-82e9-7f51d6f424e6" />


<img width="992" height="705" alt="image" src="https://github.com/user-attachments/assets/bdb86cda-4437-4a95-930b-f3c4eb155666" />

---

## References

1. Sentence-Transformers Documentation - https://www.sbert.net/
2. TF-IDF and Cosine Similarity - https://scikit-learn.org/stable/modules/feature_extraction.html
3. HuggingFace Models - https://huggingface.co/sentence-transformers





