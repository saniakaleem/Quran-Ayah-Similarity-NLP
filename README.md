# 📖 Quranic Ayah Similarity Detection using NLP, Clustering & Sentence Transformers

This project performs intelligent similarity analysis across Quranic ayahs using multiple Natural Language Processing (NLP) methods. The system allows users to input an Arabic ayah and receive similar ayahs based on:
- Exact Textual Matching (Character-level NLP)
- Clustering-based Grouping (KMeans on TF-IDF)
- Semantic Similarity using Sentence Transformers (BERT-based)

---

##  Dataset

Quranic data is sourced from a free and structured public JSON API:

**Dataset URL:**  
https://cdn.jsdelivr.net/npm/quran-json@3.1.2/dist/quran.json

Each surah and verse contains:
- `surah_name`
- `verse_id`
- `text` (ayah in Arabic)

---


##Features

| Method                        | Description                                      |
|-------------------------------|--------------------------------------------------|
| **1. NLP Cosine Similarity**  | Uses character-level n-grams & CountVectorizer  |
| **2. KMeans Clustering**      | Groups ayahs by textual patterns using TF-IDF   |
| **3. Sentence Transformer**   | Uses `asafaya/bert-base-arabic` for semantic similarity |
| **Word Cloud Visualization**  | Generates Arabic word cloud of frequent ayah terms |
| **Gradio Interface**          | Interactive GUI with separate tabs for each method |

---

##Example Interface

- Input an ayah
- See:
  - Similar ayahs based on NLP
  - Repetitions using clustering
  - Semantic matches using BERT
- Output includes:
  - Ayah text
  - Surah name and verse number
  - Similarity percentage (where applicable)
---

## Installation
```bash
pip install -r requirements.txt
pip install gradio arabic-reshaper python-bidi gensim scikit-learn matplotlib wordcloud sentence-transformers
---

Models Used
Method	Model or Technique
Exact Similarity	CountVectorizer(analyzer='char')
Clustering	KMeans on TF-IDF vectors
Semantic Similarity	asafaya/bert-base-arabic (SentenceTransformer)
 Authors
•	Sania Kaleem
•	LinkedIn
•	GitHub

## License
This project is for educational purposes under MIT License.
