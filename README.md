Instructions
Prepare Files: Save your job description in a file named job.txt and your Overleaf resume in a file named resume.txt.

Run the Script: The script will read these files, process the content, and provide an ATS score along with suggestions on how to improve your resume.

Explanation
Reading Files: read_file reads the content of the given file.
Extracting Text from LaTeX: extract_plain_text_from_latex removes LaTeX commands to get plain text.
Parsing Resume: parse_resume organizes the resume content into sections.
Finding Synonyms: find_synonyms uses spacy to find synonyms of keywords.
Calculating Score: calculate_score calculates the ATS score based on keyword matches and section weights.
Improvement Suggestions: suggest_improvements provides suggestions for missing keywords.
