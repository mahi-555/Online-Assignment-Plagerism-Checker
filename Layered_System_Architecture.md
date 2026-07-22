# Layered System Architecture

## 1. Presentation Layer (Frontend)
- Upload page (drag & drop assignment file)
- Results dashboard (score, highlighted matches)
- Report download button
- Built with React (or plain HTML/CSS/JS)

## 2. Application Layer (Backend API)
- Handles file upload requests
- Routes text to extraction and preprocessing modules
- Coordinates local + online similarity checks
- Returns final JSON result to frontend
- Built with FastAPI or Flask

## 3. AI/Processing Layer
- Text extraction (PyPDF2, python-docx, plain text parsing)
- Preprocessing: lowercasing, stopword removal, tokenization, lemmatization
- Similarity detection:
  - TF-IDF + Cosine Similarity (fast, keyword-based)
  - Sentence-BERT embeddings (semantic/meaning-based, catches paraphrasing)
- Web matching via SerpAPI/Google Custom Search + snippet comparison

## 4. Data Layer
- Stores all past submissions (for local similarity checks)
- Stores generated reports
- Stores user/student metadata
- MongoDB (flexible documents) or PostgreSQL (structured/relational)

## 5. Infrastructure Layer
- Hosting: Render / Railway / Vercel
- File storage: local disk or cloud bucket (S3/Cloudinary) for uploaded files
- Environment config via `.env` file
