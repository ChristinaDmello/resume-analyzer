# 📄 Resume Analyzer

A beginner-friendly Resume Analyzer built with Python and Flask that allows users to upload PDF or DOCX resumes and automatically extracts technical skills using keyword-based NLP techniques.

## 🚀 Features

* Upload resumes in PDF and DOCX formats
* Extract text from uploaded resumes
* Detect skills across multiple categories
* Responsive and user-friendly interface
* Privacy-focused processing
* No paid APIs required

## ⚙️ How It Works

| Layer          | What it does                                                                              |
| -------------- | ----------------------------------------------------------------------------------------- |
| **Upload**     | Flask receives the file and saves it temporarily to `uploads/`                            |
| **Extraction** | `pdfplumber` reads PDFs page-by-page; `python-docx` reads DOCX paragraphs and tables      |
| **Analysis**   | Regex word-boundary search scans the text against 120+ skill keywords across 5 categories |
| **Display**    | Results are returned as JSON; JavaScript renders color-coded skill cards                  |

## ✨ Features at a Glance

* Drag & drop or browse to select a file
* Detects 5 categories:

  * Programming Languages
  * Web Frameworks
  * Databases
  * Cloud & DevOps
  * Tools & Technologies
* Shows total skill count and category count in stat badges
* Friendly message when no skills are detected
* Files are deleted from disk immediately after processing (privacy)
* Responsive — works on mobile and desktop
* All free, no paid APIs

## 📂 Project Structure

resume-analyzer/
│
├── app.py
├── requirements.txt
├── uploads/
│
├── templates/
│   └── index.html
│
└── static/
    └── style.css

## 🛠 Installation

Step 1 — Create & activate a virtual environment (recommended)

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# Mac / Linux
source venv/bin/activate

Step 2 — Install all dependencies

```bash
pip install -r requirements.txt
Step 3 — Download the spaCy English model
```bash
python -m spacy download en_core_web_sm

Step 4 — Run the app
```bash
python app.py
```
 Step 5 — Open in your browser
```text

## 💻 Technologies Used

* Python
* Flask
* spaCy
* pdfplumber
* python-docx
* HTML
* CSS
* JavaScript

## 📌 Notes

* Supports PDF and DOCX resume formats
* Uses keyword-based NLP for skill detection
* No external or paid APIs required
* Designed as a beginner-friendly NLP and Flask project
* Suitable for academic and portfolio use
