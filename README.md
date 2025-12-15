# PDF Waybill Splitter & Grouper (Logistics Automation)

## 📌 Overview
This Python automation script processes **master PDF files containing multiple waybills**, extracts waybill numbers from each page, and splits them into **individual PDFs grouped by waybill number**.

It is designed for logistics environments where bulk PDFs must be separated and organized automatically.

---

## 🚀 Features
- Scans each PDF page and extracts waybill numbers using regex
- Groups pages belonging to the same waybill
- Creates one PDF per waybill number
- Saves unidentified pages separately for manual review
- Automatically deletes the original master PDF after processing
- Handles bulk PDF files from a folder

---

## 🛠️ Technologies Used
- Python
- pdfplumber (text extraction)
- PyPDF2 (PDF reading & writing)
- Regular Expressions (pattern matching)

---

## 📂 How Waybill Detection Works
- Waybill numbers format (configurable):
  - Start with **4, 5, or 7**
  - Be **10–15 digits long**
- Pattern used (configurable):
```text
\b[457]\d{9,14}\b
```

---

## ⚙️ Configuration
Update these paths inside the script before running:

```python
input_folder = r"PATH_TO_INPUT_PDF_FOLDER"
output_folder = r"PATH_TO_OUTPUT_PDF_FOLDER"
```

---

## ▶️ How to Run

#### 1️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

#### 2️⃣ Run the Script
```bash
python split_pdfs.py
```

---

## ⚠️ Requirements
- Windows / Linux / macOS
- Python 3.8+
- PDFs must contain selectable text (not scanned images)

---

## 📈 Use Case

#### Ideal for:
- Logistics & courier operations
- Bulk waybill PDF processing
- Document segregation and archival
- Reducing manual PDF handling time
