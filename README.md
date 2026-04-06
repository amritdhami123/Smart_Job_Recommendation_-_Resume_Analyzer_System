# Smart Job Recommendation & Resume Analyzer System

 **A practical ML + NLP system that helps job seekers match their resumes with real job roles**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B.svg)](https://streamlit.io/)

### Prerequisites
- Python 3.8 or higher
- Git installed
- Basic understanding of Python virtual environments


### Table of Contents
---
### Table of Contents
- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Setup Guide](#setup-guide)  
- [Quick Demo](#quick-demo)   
- [How to Use](#how-to-use)
- [Troubleshooting](#troubleshooting)


### About
---
In today’s competitive job market, many candidates struggle to understand why they are not getting selected. This project tackles that exact problem.

The system analyzes a resume, compares it with job descriptions, and provides:

- A matching score
- Missing skills
- Recommended job roles

The goal is simple: to help users make smarter, data-driven career decisions.

### Features
---
- Extracts text and information from resumes (PDF)
- Identifies skills using NLP techniques
- Compares resumes with job descriptions
- Generates a job match score
- Highlights skill gaps clearly
- Suggests relevant job roles
- Optional web interface for interactive use

### Tech Stack
---
This project is built using:

- Python
- Pandas & NumPy (data handling)
- Scikit-learn (ML models)
- TF-IDF & Cosine Similarity (text matching)
- SpaCy / NLTK (NLP processing)
- Streamlit / Heroku
- Jupyter Notebook (experiments)


### Project Structure
---
```
 Smart_Job_Recommendation_-_Resume_Analyzer_System /
 ├── notebook/ # Jupyter notebooks for experiments
 ├── src/ # Core Python modules (NLP + ML logic) │ ├── resume_parser.py │ ├── job_matcher.py │ └── skill_extractor.py
 ├── app.py # Streamlit web application
 ├── train.py # Model training pipeline
 ├── requirements.txt # Python dependencies
 ├── README.md # This documentation
 └── data/ # Sample resumes and job descriptions (optional)
 ```

### Quick Demo

1. Upload your resume (PDF/DOCX)
2. View your extracted skills
3. See job match scores
4. Identify skill gaps
5. Get role recommendations



### Setup Guide

#### 1. Clone the repository
```bash
git clone https://github.com/amritdhami123/Smart_Job_Recommendation_Resume_Analyzer_System.git
cd Smart_Job_Recommendation_Resume_Analyzer_System
```


#### 2. Create and activate a virtual environment (Recommended)
---
- Windows:
```
python -m venv venv
venv\Scripts\activate 
```
- macOS/Linux:
```
python3 -m venv venv
source venv/bin/activate
```

#### 3. Install dependencies
---
```
pip install -r requirements.txt
``` 

### How to Use
---
#### 1. Train the Model
```
python train.py
```

#### 2. Run the Application 
---
```
streamlit run app.py
```

### Output
---
- Resume analysis
- Job match score
- Missing skills
- Suggested roles

### Project Highlights
---
- Solves a real-world problem for job seekers  
- Demonstrates an end-to-end ML pipeline  
- Combines NLP, Machine Learning, and deployment concepts  
- Designed to scale for real-world job platforms

### Future Improvements

- Integrate real-time job APIs (LinkedIn, Indeed)
- Improve skill extraction using deep learning models
- Add user authentication and profile tracking
- Deploy on cloud for public access

### Support
For questions or issues, please:
1. Check the [Issues](https://github.com/amritdhami123/Smart_Job_Recommendation_Resume_Analyzer_System/issues) page
2. Contact: - Email: amrit99dhami@gmail.com <br>
            - LinkedIn: https://www.linkedin.com/in/amritdhami123/

### Troubleshooting
---
If you encounter issues during setup or execution, try these solutions:

*   **"Module not found" errors**  
    *   **Cause:** The virtual environment is not activated or a package is missing.  
    *   **Fix:** Ensure you see `(venv)` in your terminal. If not, run `venv\Scripts\activate` (Windows) or `source venv/bin/activate` (Mac/Linux). Then run `pip install -r requirements.txt`.

*   **Streamlit command not recognized**  
    *   **Cause:** Streamlit is not installed in the current environment.  
    *   **Fix:** Run `pip install streamlit` specifically, or ensure you are inside the activated virtual environment.

*   **Resume parsing fails**  
    *   **Cause:** The uploaded file is corrupted or in an unsupported format.  
    *   **Fix:** Ensure you are uploading a clean `.pdf` or `.docx` file. If using `pdfplumber`, ensure it is installed: `pip install pdfplumber`.

*   **NLTK/SpaCy Model Errors**  
    *   **Cause:** Natural language models are not downloaded.  
    *   **Fix:** Run these commands in your terminal:  
        ```bash
        python -m spacy download en_core_web_sm
        python -m nltk.downloader punkt
        ```
