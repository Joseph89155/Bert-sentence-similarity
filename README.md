# 🤖 BERT Sentence Similarity

This project explores **semantic sentence similarity** using the **BERT transformer model** from HuggingFace. It uses contextual embeddings derived from the `[CLS]` token to compute pairwise similarity between sentence pairs using **cosine similarity**. The project includes data processing, model inference, evaluation metrics, and visualizations.

## 🔍 Real-Life Application Scenario

**Use Case: Duplicate Question Detection on a Q&A Platform**

Imagine a platform like Stack Overflow or Quora, where users often post similar or identical questions using different phrasing. Automatically detecting duplicate questions is crucial to avoid redundancy and improve content discovery.

This project simulates that scenario:
- It evaluates how BERT embeddings can detect **semantically similar questions** even if they use different words.
- A threshold-based cosine similarity approach is used to classify whether two sentences express the same meaning.

This approach is also applicable to:
- **Plagiarism detection**
- **Paraphrase identification**
- **Semantic search engines**
- **Chatbot response retrieval**
- **Legal document deduplication**

---

## 📌 Project Structure

bert-sentence-similarity/

│

├── bert_similarity.ipynb # Complete Colab/Notebook pipeline

├── README.md # Project documentation

├── requirements.txt # Required dependencies (optional)

├── /images # Output plots (similarity distribution, heatmap)

└── saved_model/ # (Optional) Saved model artifacts

---


## 🧠 What This Project Does

- Loads a list of 10 sentence pairs with known similarity labels
- Tokenizes and encodes the text using the `bert-base-uncased` model
- Extracts the `[CLS]` token embedding from BERT as the sentence representation
- Computes **cosine similarity** between sentence vectors
- Applies a **threshold** (e.g., 0.9) to classify pairs as similar/dissimilar
- Evaluates performance with **accuracy**, **precision**, **recall**, and **F1-score**
- Generates **visualizations**:
  - Cosine similarity distribution with threshold line
  - Heatmap of pairwise similarities

---

## 🛠️ Tech Stack

- Python 3.x
- HuggingFace Transformers
- PyTorch
- Scikit-learn
- Matplotlib / Seaborn
- Google Colab or Jupyter Notebook

---

## 📊 Results

| Metric     | Value |
|------------|-------|
| Accuracy   | 0.50  |
| Precision  | 0.50  |
| Recall     | 1.00  |
| F1 Score   | 0.67  |

---

## 📈 Visual Outputs

- ✅ Cosine similarity histogram with threshold marker
- ✅ Sentence similarity matrix heatmap

---

## 🧾 Conceptual Insights Covered

- BERT vs Traditional NLP (BoW, TF-IDF)
- Encoder’s role in Transformer architecture
- Contextual embeddings and semantic awareness
- Importance of `[CLS]` token for classification
- Cosine similarity as a metric for semantic distance

---

## 🚀 Future Improvements

- Fine-tune BERT on a domain-specific similarity dataset
- Integrate Sentence-BERT for better performance
- Convert to an API endpoint for production use
- Include web-based interface for sentence input and live similarity scoring

---

## 📚 References

 - BERT Paper

 - HuggingFace Transformers

 - Sentence Similarity with Transformers – Medium

---

## 👤 Author
 - Joseph Maina
 - Data Science & NLP Enthusiast

---

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details.
