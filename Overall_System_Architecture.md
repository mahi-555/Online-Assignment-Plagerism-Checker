# Overall System Architecture

```
Assignment File (PDF/DOCX/TXT)
            |
            v
      File Upload API
            |
            v
      Text Extraction Module
            |
            v
      Text Preprocessing (clean, tokenize, remove stopwords)
            |
            +----------------------------+
            |                            |
            v                            v
  Local Database Similarity    Online Source Similarity
  (TF-IDF / Cosine Similarity) (Web Search API + Scraping)
            |                            |
            +-------------+--------------+
                          |
                          v
              Similarity Scoring Engine
                          |
                          v
              Report Generator (highlighted matches)
                          |
                          v
                   Dashboard / UI
                          |
                          v
                      Database
              (store submission + report)
```

## Core Components
1. **File Upload API** – accepts PDF, DOCX, or TXT files
2. **Text Extraction Module** – pulls raw text out of the file (PyPDF2, python-docx)
3. **Preprocessing Module** – cleans and normalizes text for comparison
4. **Local Similarity Engine** – compares against previously submitted assignments
5. **Online Similarity Engine** – compares against web content via search API
6. **Scoring Engine** – combines both results into a final plagiarism percentage
7. **Report Generator** – produces a report with highlighted matching text
8. **Dashboard** – lets users upload files and view results
9. **Database** – stores submissions, scores, and reports for future comparisons
