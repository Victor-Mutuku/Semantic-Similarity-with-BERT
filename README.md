#PolysemyProbe – Dynamic BERT Embeddings

This project demonstrates how BERT captures contextual (dynamic) word meanings using sentence embeddings, token-level embeddings, and cosine similarity. It also shows how BERT handles polysemy (words with multiple meanings) based on context.
---
##Project Overview

This project uses a pre-trained BERT model (bert-base-uncased) from Hugging Face Transformers to:

Generate sentence embeddings using mean pooling or the [CLS] token.

Extract token-level contextual embeddings.

Demonstrate polysemy through context-dependent vector differences.

Compute cosine similarity between sentence pairs.

Predict semantic similarity using a threshold of 0.7.

Evaluate accuracy using a labeled dataset.
---
##Dataset

A custom dataset of 10 sentence pairs, each labeled as:

1 — semantically similar

0 — not similar

The dataset contains both realistic similarities and intentionally mismatched examples.
---
##Key NLP Concepts
**Contextual Embeddings

BERT produces dynamic embeddings where the same word has different vectors depending on context.

**Polysemy

Words such as "bank" or "python" change meaning based on usage, and BERT captures this.

**Self-Attention

BERT uses attention to understand relationships between all tokens in a sentence.

**Cosine Similarity

Measures the semantic closeness between two sentence vectors.
---
