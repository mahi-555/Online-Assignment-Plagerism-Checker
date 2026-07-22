# Phase 4: Local Database Similarity Check

## Goal
Compare a new submission against all previously stored submissions.

## Tasks
- Store every submission's cleaned text in the database
- Implement TF-IDF vectorization using `scikit-learn`
- Compute cosine similarity between the new submission and every stored document
- (Optional) Add Sentence-BERT semantic similarity for paraphrase detection
- Return the top matching submissions with similarity percentages

## Deliverable
A `local_similarity.py` module that returns a similarity score (0–100%) and a list of the most similar previous submissions.
