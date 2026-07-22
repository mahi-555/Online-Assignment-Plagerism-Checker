# Phase 5: Online Source Matching

## Goal
Check the assignment against content available online.

## Tasks
- Extract distinctive sentences/phrases from the assignment (e.g., every 3rd–5th sentence)
- Query a search API (SerpAPI or Google Custom Search API) with each phrase
- Fetch top result snippets/URLs
- Compare returned snippets against the assignment text using cosine similarity
- Track which sentences matched which URL

## Deliverable
An `online_similarity.py` module that returns an online similarity score and a list of matched URLs with matched text sections.
