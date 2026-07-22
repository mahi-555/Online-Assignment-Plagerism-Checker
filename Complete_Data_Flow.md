# Complete Data Flow

1. **User uploads file** → PDF, DOCX, or TXT via the frontend upload form.
2. **File sent to backend** → API receives file and saves it temporarily.
3. **Text extraction** → raw text pulled out based on file type.
4. **Preprocessing** → text cleaned: lowercase, remove punctuation/stopwords, tokenize, lemmatize.
5. **Parallel similarity checks:**
   - a) Compare cleaned text against all previous submissions stored in the database (local check).
   - b) Send key phrases/sentences to a web search API and compare returned snippets against the assignment (online check).
6. **Score aggregation** → local score + online score combined into one overall plagiarism percentage, with a breakdown of which sections matched which source.
7. **Report generation** → matched sentences highlighted, sources listed, final score displayed.
8. **Save to database** → submission text, score, and report stored for future comparisons and record-keeping.
9. **Response sent to frontend** → dashboard displays score, highlighted report, and downloadable PDF/summary.

## Data Stored Per Submission
- Student name / ID (optional)
- Original file
- Extracted & cleaned text
- Similarity score (local %, online %, overall %)
- Matched sources (list of URLs or previous submission IDs)
- Timestamp
