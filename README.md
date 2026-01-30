# 🌏 Evaluating Large Language Models on Khmer Language Understanding

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-orange.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-1.13-red.svg)
![NLP](https://img.shields.io/badge/NLP-LLM%20Evaluation-green.svg)
![Course](https://img.shields.io/badge/Course-MASI51NLP%202025-purple.svg)
![License](https://img.shields.io/badge/License-MIT-brightgreen.svg)
![Status](https://img.shields.io/badge/Status-Academic%20Project-orange.svg)

---

## 📘 Course Information
**MASI51NLP 2025**  
**Topic:** LLM Evaluation for Low-Resource Languages (Khmer)

---

## 🎯 Objective
This project **evaluates Large Language Models (LLMs)** on their ability to **understand and process the Khmer language**, compared with **high-resource English** and **regional languages (Thai, Vietnamese, etc.)**.

Focus areas:
- 📚 Vocabulary coverage & tokenizer behavior  
- ✂️ Tokenization efficiency (fertility test)  
- 🧠 Cross-lingual semantic alignment  
- 🔍 Model behavior (syntax vs bag-of-words)

---

## 🤖 Models Evaluated

### Model A (Khmer-Optimized)
| Model Name | HF Identifier |
|------------|---------------|
| metythorn/khmer-xlm-roberta-small | `metythorn/khmer-xlm-roberta-small` |
| metythorn/khmer-xlm-roberta-base-10k | `metythorn/khmer-xlm-roberta-base-10k` |
| Msok99/km-improved-32k | `Msok99/km-improved-32k` |
| Msok99/km-improved-22k-v4 | `Msok99/km-improved-22k-v4` |
| xlm-roberta-base | `xlm-roberta-base` |
| xlm-roberta-large | `xlm-roberta-large` |
| bert-base-multilingual-cased | `bert-base-multilingual-cased` |
| facebook/xlm-v-base | `facebook/xlm-v-base` |
| facebook/nllb-200-distilled-600M | `facebook/nllb-200-distilled-600M` |

### Model B (English-Centric)
| Model Name | HF Identifier |
|------------|---------------|
| gpt2 | `gpt2` |
| distilgpt2 | `distilgpt2` |
| roberta-base | `roberta-base` |
| bert-base-uncased | `bert-base-uncased` |
| albert-base-v2 | `albert-base-v2` |
| EleutherAI/gpt-neo-125M | `EleutherAI/gpt-neo-125M` |
| roberta-large | `roberta-large` |
| distilbert-base-uncased | `distilbert-base-uncased` |
| xlnet-base-cased | `xlnet-base-cased` |

---

## 🧪 Evaluation Tasks

### 🔹 Part 1: Vocabulary & Tokenizer Analysis
- Unicode-based script identification  
- Vocabulary share by language  
- Token length statistics  

### 🔹 Part 2: Tokenization Efficiency (Fertility Test)
- Parallel Khmer–English corpus  
- Fertility ratio comparison (Tokens ÷ Characters)  
- Boxplot visualization  

### 🔹 Part 3: Embedding Geometry & Semantics
- Static embedding extraction  
- Cosine similarity on translation pairs vs random pairs  

### 🔹 Part 4: Mechanism Analysis
- Original vs shuffled sentences  
- Cosine similarity of embeddings  
- Syntax sensitivity analysis  

---

## 📊 Key Results: Fertility Ratio Analysis

**Mean Fertility Ratio (F)**

| Model | Khmer | English |
|-------|-------|---------|
| Model A | 0.3106 | 0.4587 |
| Model B | 2.5134 | 0.2251 |

**Interpretation**
- **Model A (Khmer-Optimized)**:  
  - Efficient tokenization for Khmer (F ≈ 0.31)  
  - Balanced token lengths in English (F ≈ 0.46)  
  - Suitable for multilingual and Khmer-specific tasks
- **Model B (English-Centric)**:  
  - Very high Khmer fertility (F ≈ 2.51) → inefficient subword compression  
  - Works better for English (F ≈ 0.23)  
  - Not suitable for Khmer or low-resource languages  

---

## 🔍 Overall Observations

### Vocabulary & Tokenization
- Model A: Low fertility → better subword efficiency for Khmer  
- Model B: High fertility → relies on character-level fallback  

### Embedding Geometry
- Model A: Partial cross-lingual alignment  
- Model B: Poor Khmer alignment, English embeddings only  

### Mechanism Analysis
- Both models largely bag-of-words; Model A slightly sequence-sensitive in English  
- Model B ignores word order in Khmer  

---

## ✅ Final Model Selection (Parts 2–4)

- **Model A (`metythorn/khmer-xlm-roberta-small`)**  
  - Best for low-resource languages like Khmer and Lao  
  - Efficient tokenization, balanced embeddings, partial cross-lingual alignment  
- **Model B (`roberta-base`)**  
  - Performs well for English only  
  - Serves as a baseline for English tasks  
- **Usage:**  
  - **Tokenization, Embeddings, Attention Analysis** → Use **Model A for Khmer**  
  - **English baseline / comparison** → Use **Model B**  

> **Conclusion:** Model A is superior for Khmer/Lao; Model B only as English reference.

---

## 👥 Team AMS-5-C

### 👨‍🏫 Instructor / Teacher
| Avatar | Name | GitHub |
|--------|------|--------|
| <img src="https://github.com/VannyKhon.png" width="48"/> | **Vanny Khon** | [VannyKhon](https://github.com/VannyKhon) |

### 🧑‍💻 Students
| Avatar | Name | GitHub |
|------|------|--------|
| <img src="https://github.com/AhLang03.png" width="48"/> | **Srun Kimlang** | [AhLang03](https://github.com/AhLang03) |
| <img src="https://github.com/Lyhour7777.png" width="48"/> | **SEM YUTHEARYLYHOUR** | [Lyhour7777](https://github.com/Lyhour7777) |
| <img src="https://github.com/mengsoklin.png" width="48"/> | **Veng Mengsoklin** | [mengsoklin](https://github.com/mengsoklin) |
| <img src="https://github.com/meyseav.png" width="48"/> | **Vorn Seavmey** | [meyseav](https://github.com/meyseav) |
| <img src="https://github.com/MunineathSek.png" width="48"/> | **Sek Munineath** | [MunineathSek](https://github.com/MunineathSek) |
| <img src="https://github.com/Natt2509.png" width="48"/> | **Sorn Sreynatt** | [Natt2509](https://github.com/Natt2509) |
| <img src="https://github.com/RozaVong.png" width="48"/> | **Vang Roza** | [RozaVong](https://github.com/RozaVong) |
| <img src="https://github.com/Ton-chamnan.png" width="48"/> | **Ton Chamnan** | [Ton-chamnan](https://github.com/Ton-chamnan) |
| <img src="https://github.com/vannajuuka.png" width="48"/> | **Vanna Juuka** | [vannajuuka](https://github.com/vannajuuka) |
| <img src="https://github.com/sreypich999.png" width="48"/> | **Vey Sreypich** | [sreypich999](https://github.com/sreypich999) |


---

## 📦 Technologies & Libraries
- 🐍 **Python 3.8+**  
- 🤗 **Hugging Face Transformers**  
- 🛠️ **PyTorch**  
- 📊 **NumPy & Pandas**  
- 📈 **Matplotlib & Seaborn**  
- ☁️ **Google Colab**

---

## 📄 Deliverables
- Google Colab notebook with **well-commented Python code**  
- Vocabulary & tokenization histograms  
- Fertility ratio boxplots  
- Concise comparative summary (≤ 300 words)  

---
---

## 🔗 Colab Notebook
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1PwFSgGDAoPPID5TwVY-0n3vVZDtOOqQ9#scrollTo=DA_UJdCE_lsY)

