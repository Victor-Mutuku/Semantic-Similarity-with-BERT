# PolysemyProbe – Dynamic BERT Embeddings

## Project Overview
This project explores how **BERT generates contextual word and sentence embeddings**, demonstrating how meaning shifts based on context (polysemy). The workflow includes **sentence encoding, token-level embedding extraction, cosine similarity computation**, and accuracy evaluation on a custom dataset of sentence pairs.

---

## Dataset
- **Source:** Custom sentence-pair list  
- **Pairs:** 10  
- **Labels:**  
  - 1 = semantically similar  
  - 0 = not similar  
- **Features:** Two sentences + similarity label  
- Includes both **real semantic pairs** and intentionally **contradictory / mismatched** ones.

---

## Workflow & Detailed Steps

### 1. Loading BERT
- Loaded **BERT tokenizer** and **TFBertModel** (`bert-base-uncased`) from Hugging Face.  
- Tokenized each sentence into input IDs and attention masks.  
- Passed inputs through BERT to obtain contextual embeddings.

### 2. Sentence Embedding Extraction
- **[CLS] Token Embedding:** Represents the entire sentence.  
- **Mean Pooling (used in final run):** Average of all token embeddings to get sentence-level embedding.

### 3. Cosine Similarity Computation
- Obtained embeddings for each sentence pair.  
- Computed similarity using `cosine_similarity(embedding1, embedding2)`.  
- Applied threshold: similarity > 0.7 → 1, otherwise → 0.

### 4. Prediction & Evaluation
- Generated predictions (`0`/`1`) for each pair.  
- Compared predictions against ground-truth labels.  
- Calculated model accuracy.

### 5. Output
- Printed similarity score, predicted label, and evaluation accuracy.

---

## Key NLP Concepts

### Contextual Embeddings
BERT produces **dynamic embeddings**, where the same word has different vectors depending on context.

### Polysemy
Words such as *bank* or *python* change meaning based on usage, and BERT captures this.

### Self-Attention
BERT uses attention mechanisms to understand relationships between all tokens in a sentence.

### Cosine Similarity
Measures the **semantic closeness** between two sentence embeddings.

---

## Skills Demonstrated
- **Transformer-based NLP:** Hugging Face Transformers  
- **Sentence Encoding:** CLS vs mean pooling  
- **Similarity Measurement:** cosine similarity  
- **Contextual Embedding Analysis:** handling polysemy  
- **Model Evaluation:** accuracy scoring  
- **TensorFlow Model Execution:** running TFBertModel on text  

---

## Outputs & Insights
- Extracted **dynamic, context-aware embeddings** from BERT.  
- Demonstrated BERT can identify **semantically similar sentences**.  
- Unrelated sentences yield low similarity scores.  
- Achieved strong accuracy on the small dataset.  
- Validated that **BERT captures semantic relationships** better than static vectors.

---
