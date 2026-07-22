# AI Processing Pipeline

## Step 1: Text Extraction
- PDF → PyPDF2 / pdfplumber
- DOCX → python-docx
- TXT → direct read

## Step 2: Preprocessing
- Convert to lowercase
- Remove punctuation, special characters
- Remove stopwords (NLTK/spaCy stopword list)
- Tokenization (split into words/sentences)
- Lemmatization (reduce words to root form)

## Step 3: Similarity Detection

### Method A — TF-IDF + Cosine Similarity (fast, keyword-level)
- Convert documents into TF-IDF vectors using scikit-learn
- Compute cosine similarity between the new submission and each stored document
- Good for catching direct copy-paste

### Method B — Semantic Similarity (Sentence-BERT)
- Encode sentences into embeddings using `sentence-transformers`
- Compare embeddings using cosine similarity
- Good for catching paraphrased/reworded plagiarism

## Step 4: Online Source Matching
- Extract distinctive phrases/sentences from the assignment
- Query a search API (SerpAPI/Google Custom Search) with those phrases
- Compare returned snippets against the assignment text using the same similarity methods

## Step 5: Score Aggregation
- Weighted combination of local DB score + online score
- Example: `final_score = (0.4 * local_score) + (0.6 * online_score)`

## Step 6: Highlighting
- Mark matched sentences/phrases in the report
- Attach the matching source (URL or submission ID) to each highlighted section
