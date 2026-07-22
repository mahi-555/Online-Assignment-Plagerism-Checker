# Phase 6: Scoring & Report Generation

## Goal
Combine local and online results into a final report.

## Tasks
- Aggregate local score + online score into one overall plagiarism percentage
  - Example weighting: `final_score = (0.4 * local_score) + (0.6 * online_score)`
- Generate a report showing:
  - Overall similarity percentage
  - Highlighted matched sentences (color-coded by source)
  - List of matched sources (previous submission IDs / URLs)
- Export report as downloadable PDF or HTML

## Deliverable
A `report_generator.py` module that outputs a complete plagiarism report given the local and online similarity results.
