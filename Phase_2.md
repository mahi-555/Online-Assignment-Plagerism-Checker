# Phase 2: File Upload & Text Extraction

## Goal
Allow users to upload an assignment file and extract the raw text.

## Tasks
- Build a file upload API endpoint (`POST /upload`)
- Accept PDF, DOCX, and TXT files
- Extract text:
  - PDF → `PyPDF2` or `pdfplumber`
  - DOCX → `python-docx`
  - TXT → direct file read
- Validate file type and size
- Return extracted raw text as JSON response (for testing)

## Deliverable
Uploading a file returns the correctly extracted plain text in the API response.
