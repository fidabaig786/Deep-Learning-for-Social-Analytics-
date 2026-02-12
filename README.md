# Deep-Learning-for-Social-Analytics-
ESESG Topic Modeling &amp; LLM-Enhanced Labeling
# ESG Topic Modeling & LLM-Enhanced Labeling

A research-driven Natural Language Processing (NLP) project that applies **BERTopic**, transformer embeddings, and **LLM-based topic labeling** to analyze ESG-related textual data.

This project explores how unsupervised topic modeling combined with Large Language Models (LLMs) can improve interpretability and semantic quality of extracted topics.

---

##  Project Overview

The goal of this project is to:

- Extract meaningful topics from ESG-related documents  
- Evaluate topic quality using coherence and diversity metrics  
- Improve topic interpretability using LLM-based labeling  
- Analyze actor-topic relationships (e.g., politicians, firms)  
- Provide structured insights before predictive modeling  

This project was developed as part of an advanced research workflow in NLP and social analytics.

---

## 🏗️ Methodology

The pipeline consists of four major phases:

### Data Preparation
- Merge multiple ESG datasets  
- Remove duplicates  
- Text preprocessing  
- Vectorization using `CountVectorizer`  

### Embedding & Topic Modeling
- Sentence embeddings via `SentenceTransformer`  
- Dimensionality reduction using `UMAP`  
- Clustering via `HDBSCAN`  
- Topic extraction using `BERTopic`  

### 3️⃣ Topic Evaluation

We evaluate topic quality using:

- **Topic Coherence (c_v)**  
- **Topic Diversity**  
- **Coverage & Noise Ratio**  
- **Cluster Persistence**  

This ensures model robustness before interpretation.

### 4️⃣ LLM-Based Topic Labeling

To improve interpretability, we:

- Extract top keywords per topic  
- Send them to an LLM  
- Generate semantically meaningful labels  

This significantly improves topic clarity compared to keyword-only labeling.

---

##  Technologies Used

- Python  
- Pandas & NumPy  
- Scikit-learn  
- SentenceTransformers  
- BERTopic  
- UMAP  
- HDBSCAN  
- Gensim (Coherence Evaluation)  
- OpenAI API (LLM Labeling)  

---

## Example Output

| Topic ID | Top Keywords | LLM Label |
|-----------|--------------|------------|
| 0 | climate, climate change, carbon, emissions | Climate Policy & Environmental Regulation |
| 1 | stock, rating, company, investment | Financial Performance & ESG Investment |
| -1 | (noise cluster) | Outliers / Mixed Topics |

---

## Evaluation Metrics

- **Coherence (c_v)** – Measures semantic similarity between topic words  
- **Topic Diversity** – Measures uniqueness of top keywords  
- **Noise Ratio** – Percentage of documents assigned to outlier cluster (-1)  
- **Cluster Persistence** – Stability of clusters  

These metrics guide hyperparameter tuning (`min_cluster_size`, `min_samples`, `n_neighbors`).

