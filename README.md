# Computer-Vision-ocr
# 📄 OCR Document Processing & Data Extraction System

🚀 **Industry-Level AI Project using Computer Vision + Machine Learning**

This project implements an end-to-end **OCR-based document understanding system** that can:

* Extract text from scanned documents
* Classify document types automatically
* Identify key structured fields (like invoice number, date, amount, etc.)
* Provide a deployable frontend using Streamlit

---

## 📌 Project Overview

Organizations handle thousands of documents daily (invoices, reports, emails, forms, etc.). Manual processing is slow, error-prone, and costly.

This system solves that by combining:

* 🧠 Machine Learning (for document classification)
* 👁️ Computer Vision (for preprocessing)
* 🔤 OCR (Optical Character Recognition)
* 📊 NLP techniques (TF-IDF for feature extraction)

---

## 🗂️ Dataset

* **Name:** Tobacco3482
* **Source:** Kaggle
* **Size:** 3,482 scanned document images
* **Classes (10):**

  * Letter
  * Email
  * Resume
  * Scientific
  * Note
  * News
  * Memo
  * Advertisement
  * Form
  * Report

---

## ⚙️ Tech Stack

### 🔹 Languages & Libraries

* Python
* OpenCV
* Tesseract OCR
* Scikit-learn
* Pandas, NumPy
* Matplotlib, Seaborn
* Streamlit

### 🔹 Concepts Used

* Image preprocessing (denoising, binarization, deskewing)
* OCR text extraction
* TF-IDF vectorization
* Machine Learning classification
* Regex-based information extraction

---

## 🏗️ Project Architecture

```
Input Image
     ↓
Image Preprocessing (OpenCV)
     ↓
OCR Extraction (Tesseract)
     ↓
Text Processing (Cleaning + TF-IDF)
     ↓
Document Classification (ML Models)
     ↓
Field Extraction (Regex)
     ↓
Output (JSON / UI / CSV)
```

---

## 🔍 Features

✅ Image preprocessing pipeline for better OCR accuracy
✅ OCR with confidence scoring
✅ Multi-model classification:

* Naive Bayes
* Support Vector Machine (SVM)
* Random Forest

✅ Automatic best model selection
✅ Structured data extraction using regex
✅ Batch processing support
✅ Streamlit web interface
✅ Export results (CSV / JSON)

---

## 📊 Model Performance

The system evaluates multiple ML models and selects the best based on accuracy.

Metrics used:

* Accuracy
* Precision
* Recall
* F1-score
* Cross-validation score

📈 Visual outputs include:

* Confusion matrix
* Model comparison chart
* Cross-validation scores
* Per-class F1 scores

---

## ▶️ How to Run

### 🔹 Option 1: Google Colab (Recommended)

1. Open Google Colab
2. Upload or paste the notebook
3. Run all cells in order
4. Upload `kaggle.json` when prompted
5. Dataset downloads automatically

---

### 🔹 Option 2: Local Setup

#### Install dependencies:

```bash
pip install pytesseract opencv-python-headless pillow scikit-learn pandas matplotlib seaborn streamlit
```

#### Install Tesseract:

```bash
sudo apt install tesseract-ocr
```

#### Run the pipeline:

```bash
python your_script.py
```

---

## 🌐 Streamlit Frontend

Launch the web app:

```bash
streamlit run app.py
```

### Features:

* Upload document image
* View extracted text
* See predicted document type
* Extract structured fields
* Download results as JSON

---

## 📁 Project Structure

```
ocr_project/
│
├── dataset/
│   └── processed/
│
├── models/
│   └── classifier.pkl
│
├── outputs/
│   ├── confusion_matrix.png
│   ├── model_comparison.png
│   ├── cv_scores.png
│   ├── per_class_f1.png
│   └── model_metrics.csv
│
├── logs/
│
├── app.py
├── README.md
└── notebook / script
```

---

## 📦 Sample Output

```json
{
  "file": "invoice_001.jpg",
  "doc_type": "invoice",
  "clf_confidence": 0.94,
  "ocr_confidence": 0.88,
  "fields": {
    "invoice_number": "INV12345",
    "date": "12/05/2024",
    "amount": "2500.00"
  }
}
```

---

## 🚀 Future Improvements

* Deep learning-based OCR (e.g., EasyOCR / TrOCR)
* Named Entity Recognition (NER) using transformers
* Multi-language document support
* Layout-aware models (LayoutLM)
* Deployment using Docker / Cloud

---

## 🎯 Conclusion

This project demonstrates a **complete real-world AI pipeline** integrating:

* Computer Vision
* OCR
* Machine Learning
* Information Extraction

It is highly applicable in industries like:

* Finance
* Legal
* Healthcare
* Enterprise document management

---

## 👨‍💻 Author

**FZ**
Master’s in Data Science

---

## ⭐ Acknowledgements

* Kaggle for dataset
* Open-source libraries (OpenCV, Tesseract, Scikit-learn)

---

## 📌 License

This project is for educational and research purposes.
