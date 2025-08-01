## Named-Entity-Recognition
This project uses NLP techniques to extract structured information from unstructured resume documents. It identifies and extracts the following fields:

Name

Skills

Degree

Institutions

Work Experience

## Overview
The pipeline uses SpaCy, NLTK, and pdfplumber to:

Load and read PDF or TXT resumes

Preprocess and extract raw text

Use NER (Named Entity Recognition) and keyword matching to identify entities

Output structured data in dictionary format

## Input
The system accepts:

.pdf resumes using pdfplumber

.txt resumes using basic text reading

## Output
A dictionary with keys:
```
{
  "Name": "John Doe",
  "Skills": ["python", "machine learning", ...],
  "Degree": ["b.tech", "m.tech", ...],
  "Institutions": ["IIT Bombay", "Infosys"],
  "Experience": ["Led a team...", "Worked as a designer...", ...]
}
```

## Installation
Install required libraries:
```
bash
pip install spacy pdfplumber nltk
python -m spacy download en_core_web_sm
```

Also download NLTK tokenizer:
```
import nltk
nltk.download('punkt')
```
## Usage
Upload your .pdf or .txt resume.

Run the notebook.

The extracted structured data will be printed.

## Techniques Used
SpaCy NER (en_core_web_sm)

Phrase matching for known skills and degrees

PDF text extraction with pdfplumber

Sentence-level filtering for work experience

