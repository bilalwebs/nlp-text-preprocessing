<div align="center">

# Text Preprocessing with NLTK

**Natural Language Processing | Lecture 03 Activity**

A step-by-step Google Colab notebook covering tokenization, text cleaning, stop word removal, stemming and lemmatization.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-3.x-green)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Platform](https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab&logoColor=white)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/nlp-text-preprocessing/blob/main/RollNo_Muhammad_Bilal_Hussain_Activity3.ipynb)

</div>

---

## Overview

This project applies the preprocessing techniques from **NLP Lecture 03 (NLP Toolkits and Preprocessing Techniques)** to a real paragraph and shows how each step changes the data. Every task in the notebook contains its code, its output and a short comment.

## Tasks Covered

| # | Task | Tools Used |
|---|------|-----------|
| 1 | Sentence tokenization | `sent_tokenize` |
| 2 | Word tokenization | `word_tokenize` |
| 3 | Regular expression tokenization | `RegexpTokenizer` |
| 4 | Text cleaning (lowercase, punctuation, numbers) + bonus `lambda`/`map` | `re`, `string` |
| 5 | Stop word removal and frequency comparison | `stopwords`, `Counter` |
| 6 | Stemming comparison table | `PorterStemmer`, `LancasterStemmer`, `SnowballStemmer` |
| 7 | Lemmatization and comparison with stemming | `WordNetLemmatizer` |
| 8 | Reflection | - |

## Key Findings

- `sent_tokenize` handled the abbreviation **"Dr."** correctly and found all 5 sentences.
- `word_tokenize` splits contractions (*weren't* becomes *were* + *n't*) and treats punctuation as separate tokens.
- Stop word removal reduced the cleaned text from **60 to 33 tokens** and exposed the meaningful words (*experiments*, *plants*, *results*).
- Stemmers produced non-words such as `studi`, `experi` and `temperatur`; the lemmatizer returned real words such as `study`, `experiment` and `temperature`.

## Project Structure

```
nlp-text-preprocessing/
├── RollNo_Muhammad_Bilal_Hussain_Activity3.ipynb   # Main notebook (with outputs)
├── requirements.txt
├── .gitignore
└── README.md
```

## How to Run

### Option 1: Google Colab (recommended)
Click the **Open In Colab** badge at the top, then choose **Runtime > Run all**. No installation is needed.

### Option 2: Locally
```bash
git clone https://github.com/YOUR_USERNAME/nlp-text-preprocessing.git
cd nlp-text-preprocessing
pip install -r requirements.txt
jupyter notebook
```
The notebook downloads the required NLTK resources (`punkt_tab`, `stopwords`, `wordnet`, `omw-1.4`) automatically in its first cell.

## Dataset

The notebook uses the paragraph provided in the activity sheet (Option A):

> Dr. Ahmed's students are running 5 experiments in the lab on 12 March 2025! They were studying the effects of temperature (25°C and 40°C) on plants. ...

## Author

**Muhammad Bilal Hussain**
Portfolio: [bilalforge.vercel.app](https://bilalforge.vercel.app)

## Acknowledgements

Course material: *Natural Language Processing*, Lecture 03, SMIU Karachi. Reference: Bird, Klein and Loper, *Natural Language Processing with Python* (O'Reilly, 2009).
