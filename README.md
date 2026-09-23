# ⚡ GT-Invoice Extraction — Enterprise AI Platform

> **Multi-Format OCR · spaCy NLP · Image & PDF Invoice Intelligence · Automated Financial Audit · Streamlit Dashboard**

---

## 🌟 Platform Overview

**GT-Invoice Extraction** is an enterprise-grade AI invoice processing and entity extraction platform. It seamlessly ingests invoice documents in **both image formats (PNG, JPG, JPEG, TIFF, BMP, WEBP)** and **PDF documents (single/multi-page)**, applying advanced computer vision (OpenCV), OCR (Tesseract / PyMuPDF), and NLP entity recognition (spaCy + Regex Engine).

---

## 📁 Repository Structure

```
invoice-ai-platform/
├── app.py                         ← Main Streamlit Enterprise Dashboard (GT-Invoice Extraction)
├── GT_Invoice_Extraction.ipynb    ← Primary Jupyter Notebook Launcher
├── InvoiceAI_Platform.ipynb       ← Secondary Notebook Launcher
└── README.md                      ← Documentation & User Guide
```

---

## 🚀 Quick Start Guide

### 1. Launch via Jupyter Notebook
Open Jupyter Notebook or Jupyter Lab:
```bash
jupyter notebook GT_Invoice_Extraction.ipynb
```
- **Cell 1**: Auto-installs all required dependencies (`streamlit`, `plotly`, `spacy`, `pytesseract`, `opencv-python`, `PyMuPDF`, etc.).
- **Cell 2**: Executes standalone GT extraction engine on sample invoice data.
- **Cell 3**: Launches the full interactive Streamlit dashboard at `http://localhost:8501`.

### 2. Launch directly via CLI
```bash
pip install streamlit plotly pandas numpy Pillow pytesseract opencv-python PyMuPDF spacy
python -m spacy download en_core_web_sm
streamlit run app.py
```

---

## 🎯 Key Features & Analysis Capabilities

1. **Multi-Format Document Support**:
   - High-resolution Images (`PNG`, `JPG`, `JPEG`, `TIFF`, `BMP`, `WEBP`).
   - Single & Multi-Page `PDF` documents with automatic fallback between digital text & OCR.
2. **Comprehensive Entity Extraction Matrix**:
   - Invoice Number, Issue Date, Due Date, Vendor Name, Customer Name, Vendor Tax ID/VAT, PO Number, Subtotal, Taxes, Discounts, Total Amount, Email, Phone, Website, Bank Account Number.
3. **Itemized Line Item Parsing**:
   - Parses item descriptions, quantities, unit prices, and calculates itemized totals automatically.
4. **Automated Financial Audit & Risk Assessment**:
   - Mathematical check: Verifies if `Subtotal - Discount + Tax == Total Amount`.
   - Risk Scoring Engine: Calculates risk level (`LOW RISK`, `MEDIUM RISK`, `HIGH RISK`) based on missing compliance fields or math discrepancies.
5. **Interactive UI & Visual Analysis**:
   - Executive Dashboard with KPI metrics & Plotly charts.
   - Interactive Extracted Entities Matrix & spaCy NER mapping.
   - Master Invoice Repository & Data Export in **JSON, CSV, and Raw Text**.
