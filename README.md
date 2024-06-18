# Resume Matching ATS Script

This project contains a Python script that simulates an Applicant Tracking System (ATS) to match resumes against a given job description. The script processes multiple resume files, evaluates their relevance to the job description, and provides suggestions to improve the scores.

## Features

- **Keyword Extraction:** Extracts keywords from the job description using SpaCy.
- **Resume Parsing:** Parses resumes to identify and categorize relevant information.
- **Scoring:** Calculates a score for each resume based on keyword matching.
- **Suggestions:** Provides keyword suggestions to improve the resume score.
- **Batch Processing:** Processes multiple resume files and identifies the best matching resume.

## Requirements

- Python 3.6+
- SpaCy
- Scikit-learn
- NumPy

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/resume-matching-ats.git
    cd resume-matching-ats
    ```

2. **Set up a virtual environment (optional but recommended):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Download the SpaCy model:**

    ```bash
    python -m spacy download en_core_web_md
    ```

## Usage

1. **Prepare the job description and resume files:**
    - Save the job description in a file named `job.txt`.
    - Save resumes in files with names containing the word "resume" and having a `.txt` extension (e.g., `resume_1.txt`, `resume_2.txt`).

2. **Run the script:**

    ```bash
    python ats_script.py
    ```

3. **View the results:**
    - The script will output the scores for each resume and identify the best matching resume.
    - It will also provide keyword suggestions to improve the best matching resume.

## Files

- `ats_script.py`: The main script for processing and scoring resumes.
- `job.txt`: The job description file.
- `*resume*.txt`: The resume files to be processed.
- `requirements.txt`: The list of required Python packages.

## Example Output




V1 Improvements:
  Semantic Similarity Calculation:
    Added calculate_semantic_similarity function using cosine similarity to compare vectors, allowing for partial matches based on semantic similarity.
  Advanced Keyword Matching: 
    Incorporated semantic similarity in the calculate_score function with a threshold to score similar words.
  Weighted Scoring: 
    Adjusted the scoring mechanism to weigh sections differently, reflecting common industry practices.
  Enhanced Synonym Detection: 
    Improved the find_synonyms function to find similar words using vector similarities from SpaCy's vocab.
  Granular Feedback: 
    The suggest_improvements function now suggests missing keywords based on the keyword count.
