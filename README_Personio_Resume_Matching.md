# 📄 Personio Resume Matching System (NLP)

A real-world Natural Language Processing (NLP) project that scores how well a resume matches a job description — inspired by Personio, a leading HR tech company.

---

## 🎯 Project Objective

To automate resume screening by building an intelligent matching system that compares resumes with job descriptions using NLP embeddings and cosine similarity.

---

## 🧠 Business Context

**Company:** [Personio](https://www.personio.com/)  
**Domain:** HR Tech / Applicant Tracking Systems (ATS)  
**Use Case:** Resume-to-Job Matching System  
**Problem:** Recruiters manually match resumes to job descriptions — a slow, biased, and inconsistent process.  
**Solution:** Automatically score alignment between a resume and a job description using AI.

---

## 🧰 Tech Stack

- **Language:** Python
- **Libraries:** `sentence-transformers`, `scikit-learn`, `PyMuPDF`, `numpy`
- **Model:** Sentence-BERT (`all-MiniLM-L6-v2`)
- **Similarity Metric:** Cosine Similarity
- **Platform:** Google Colab (can be deployed via Streamlit)

---

## 📁 How It Works

1. ✅ Upload a **PDF Resume**
2. ✅ Parse resume text with `PyMuPDF`
3. ✅ Embed both resume and job description using `Sentence-BERT`
4. ✅ Compute **cosine similarity**
5. ✅ Output match score + interpretation (Strong / Moderate / Weak Match)

---

## 📊 Example Output

- **Resume:** `Cheva_Kavitha_Resume.pdf`
- **JD:** Data Scientist – People Analytics at Personio
- **Match Score:** `0.47`  
- **Result:** ❌ Weak match — resume likely not aligned with JD.

---

## 💻 Run This Project (Google Colab)

### Step 1: Install Libraries

```bash
!pip install sentence-transformers PyMuPDF scikit-learn
```

### Step 2: Upload and Rename Resume

```python
from google.colab import files
uploaded = files.upload()

import os
filename = list(uploaded.keys())[0]
os.rename(filename, "resume.pdf")
```

### Step 3: Full NLP Matching Code

(See [resume_matcher.ipynb](./resume_matcher.ipynb) for full code)

---

## 🔍 Score Interpretation

| Match Score | Meaning                  |
|-------------|--------------------------|
| 0.75 - 1.00 | ✅ Strong Match           |
| 0.50 - 0.74 | 🟡 Moderate Match         |
| 0.00 - 0.49 | ❌ Weak Match             |

---

## 📈 Future Enhancements

- Score multiple resumes at once
- Highlight matched/unmatched keywords
- Build a Streamlit UI for public use
- Integrate with ATS systems (e.g., Personio)

---

## 📄 PDF Report

📎 [Download full 16-page report](./Personio_Resume_Matching_Report_Venkata.pdf)

---

## 👤 Author

**Venkata Sandeep Kumar Reddy**  
Aspiring Data Scientist | Building real-world AI solutions  
📫 LinkedIn: [linkedin.com/in/venkata-ai](#)  
🌍 Portfolio: *Coming soon*

---

## 🗣️ LinkedIn Post Template

```text
🚀 Built a Resume Matching System inspired by Personio (Germany 🇩🇪)

It scores how well a resume matches a job description using NLP embeddings and cosine similarity.

✅ Tools: Python, SBERT, Cosine Similarity, PyMuPDF  
📊 Match Score Output: Strong / Moderate / Weak fit  
🧠 Real-world problem solved: resume screening for HR

Open to remote or visa-sponsored Data Science roles!  
#OpenToWork #DataScience #GermanyJobs #NLP #AIProjects
```

---

## 📎 License

MIT – Free to use, modify, and deploy.