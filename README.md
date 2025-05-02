## 🧠 Project Overview

**NEXTGENRESUME** is a research-backed resume classification system using Large Language Models, specifically **DistilBERT**, to align resumes with job descriptions in a smart, scalable, and explainable way. This work improves the traditional hiring pipeline by extracting key resume features, generating embeddings, and scoring relevance using **cosine similarity**.

> 🔁 **Inspired by** and adapted from [CV-JD-Matching by @avr2002](https://github.com/avr2002/CV-JD-Matching)

---

## 🗂️ Project Structure

```
NEXTGENRESUME/
├── main.py                       # Main script for end-to-end classification pipeline
├── pdf_extraction.py            # Extracts text, skills, and education from PDFs
├── extracted_data.csv           # Sample output CSV with skills and education
├── assets/
│   └── Drive_Link.txt           # Contains Google Drive link to job description dataset
├── requirements.txt             # Python dependencies
└── README.md                    # You're reading it!
```

> 📁 Additional datasets (resumes + job descriptions) can be accessed here:
> 📎 [Google Drive – Resume & JD Samples](https://drive.google.com/drive/folders/15fEWSFrWetXGnG2rO7PNwIoL3UFUl0zT?usp=drive_link)

---

## 🚀 Features

* 📄 Resume parsing from PDF using `pdfplumber`
* 🧠 Skill and Education extraction using custom rules + regex
* 🔤 Embedding generation via **DistilBERT**
* 📈 Resume-JD scoring using **Cosine Similarity**
* 🔎 SHAP for explainability (optional extension)
* 📊 Final output: Top-N matching resumes per JD

---

## ⚙️ Installation

```bash
git clone https://github.com/yourusername/NEXTGENRESUME.git
cd NEXTGENRESUME
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

---

## 🛠️ Usage

### 1. Extract Resume Info from PDF

```bash
python pdf_extraction.py --input_folder data/resumes --output_csv extracted_data.csv
```

### 2. Run Classification Pipeline

```bash
python main.py --resumes_csv extracted_data.csv --job_desc_file data/job_descriptions.txt
```

> Outputs: Ranked resume list with cosine similarity scores for each job description.

---

## 📊 Performance 

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 94% |
| Precision | 89.7% |
| Recall    | 91.2% |
| F1-Score  | 90.4% |

---

## 📈 Future Enhancements

* 🧠 Fine-tuning on domain-specific corpora
* 🌐 Web-based recruiter dashboard
* 🧮 Integrating explainability tools like SHAP
* 🧹 Resume image OCR with CV + NLP

---

## 📄 License

This project is licensed under the **MIT License**.
Special thanks to [CV-JD-Matching](https://github.com/avr2002/CV-JD-Matching) for the original idea base.

---

## 👩‍💻 Contributors

* **Bhavya Srujana Chinda**
* **Dandamudi Naga Kavya**
* **Chittineni Mounika**
* **Done Chandanasri**
