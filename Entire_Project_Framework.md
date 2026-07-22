# Entire Project Framework (Folder Structure)

```
plagiarism-checker/
│
├── backend/
│   ├── app.py                  # FastAPI/Flask entry point
│   ├── extraction/
│   │   ├── pdf_extractor.py
│   │   ├── docx_extractor.py
│   │   └── txt_extractor.py
│   ├── preprocessing/
│   │   └── text_cleaner.py
│   ├── similarity/
│   │   ├── local_similarity.py     # TF-IDF / cosine similarity
│   │   ├── semantic_similarity.py  # Sentence-BERT
│   │   └── online_similarity.py    # Web search API matching
│   ├── scoring/
│   │   └── score_aggregator.py
│   ├── report/
│   │   └── report_generator.py
│   ├── database/
│   │   └── db.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── UploadForm.jsx
│   │   │   ├── ResultCard.jsx
│   │   │   └── ReportView.jsx
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   └── Dashboard.jsx
│   │   └── App.jsx
│   └── package.json
│
├── docs/
│   ├── Overall_System_Architecture.md
│   ├── Layered_System_Architecture.md
│   ├── Complete_Data_Flow.md
│   ├── AI_Processing_Pipeline.md
│   ├── Complete_Development_Roadmap.md
│   └── Phase_1.md ... Phase_8.md
│
├── .env.example
├── README.md
└── .gitignore
```
