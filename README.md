# Multilingual Neural Machine Translation for North-Eastern Low-Resource Languages

This repository contains the datasets and trained models for our research paper:

**"A Multilingual Neural Machine Translation Model for English ↔ Assamese, Nepali, Bodo, Khasi, Manipuri, and Mizo"** (2025, Springer Nature).

---

## 🌍 Supported Languages

- Assamese (as)
- Nepali (ne)
- Bodo (brx)
- Khasi (kha)
- Manipuri (mni)
- Mizo (lus)

### Translation Directions
- **English → Indic**
- **Indic → English**

---

## 📂 Repository Structure

- `dataset/` – Parallel corpora for English ↔ Indic languages
- `models/` – Trained translation models
  - `English2Indic/`
  - `Indic2English/`

---

## 📊 Datasets

The `dataset/` folder contains cleaned parallel corpora for all six languages.  
Format: **Tab-separated values (TSV)** and **Comma-separated values (CSV)** with two columns:

**Corpus sources (original & used):**
- IndicTrans2, PMIndia, TDIL, Indic-mt task (WMT/related corpora) and in-house curation. 

**Preprocessing steps performed** (applied to all corpora before tokenization):  
- Remove extraneous characters (URLs, non-text noise), convert to lowercase, preserve punctuation, remove numeric noise as appropriate. 

**Tokenization & subword units:**  
- Word tokenization via NLTK (`word_tokenize`) for initial splitting; **Byte-Pair Encoding (BPE)** subword tokenization trained jointly across English + Indic languages to handle orthographic overlap and reduce OOVs. :contentReference[oaicite:12]{index=12}


---

## 🚀 Models

The `models/` folder contains trained Transformer-based NMT models:

- **English2Indic/**

- **Indic2English/**

## Evaluation metrics 

**Metrics used:** BLEU, sacreBLEU, ROUGE, METEOR, TER. These complementary metrics provide n-gram precision (BLEU), standardized BLEU (sacreBLEU), recall/overlap (ROUGE), synonym/stemming aware measure (METEOR), and edit-based error rate (TER). 


---

## 📜 License
MIT License © [Your Name or GitHub Handle]. Include per-file attribution for dataset sources where required (e.g., PMIndia, IndicTrans2, TDIL, WMT Indic-MT task links).

