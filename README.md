# Vietnamese Text Summarization & Machine Translation  

This project explores how modern NLP models can **summarize Vietnamese text** and **translate English ↔ Vietnamese**, while also experimenting with how **Reinforcement Learning (RL)** can improve model quality and output stability.

The goal of this project is to deeply understand:
- How machine translation systems are built from scratch  
- How text summarization models work  
- How Transformer-based models (GPT, Encoder–Decoder) behave  
- How RL (PPO, REINFORCE, etc.) can be applied to NLP tasks  

---

## 🚀 Features & Objectives

### 🔹 1. Machine Translation (EN → VI)
- Build translation models using:
  - **Transformer (Encoder–Decoder)**
  - **GPT-style Decoder-only models**
- Compare:
  - **Pretrained models** vs. **Training from scratch**
- Evaluate using:
  - BLEU  
  - ROUGE-1 / ROUGE-2 / ROUGE-L  

---

### 🔹 2. Vietnamese Text Summarization
- Sequence-to-sequence architecture for abstractive summarization
- Experiments with:
  - Transformer for summarization  
  - GPT finetuning for summary generation  
  - RL-based optimization (reward shaping, PPO-style training demo)

---

### 🔹 3. Reinforcement Learning Experiments
Understanding how RL interacts with NLP models:
- REINFORCE  
- PPO (Proximal Policy Optimization)  
- A2C / A3C (theoretical exploration)
- Reward modeling
- Generating improved summaries using RL-style feedback loops  

---

## 📊 Dataset

This project uses a combination of:
- **OPUS parallel corpus** (English–Vietnamese)  
- **Synthetic data generated using LLMs**  
- Custom preprocessing:
  - Tokenization  
  - Byte Pair Encoding (BPE)  
  - Train/Validation/Test splitting  

Processed datasets:
en_sents_dataset.txt
vi_sents_dataset.txt

---

## 🏗️ Model Architectures

### 🔹 Transformer (Seq2Seq)
- Encoder–Decoder  
- Multi-head self-attention  
- Positional encoding  
- Cross-attention for translation  
- Works for both summarization & translation tasks  

### 🔹 GPT (Decoder-only)
- Causal language modeling  
- Left-to-right attention  
- Fine-tuned for EN→VI translation  
- Adapted for abstractive text summarization  

### 🔹 RL-enhanced Summarization
- Policy gradient updates  
- Reward = summary quality score  
- Experimental PPO loop for summary refinement  

---

## 📈 Experimental Results (Summary)

| Model | Task | Pretrained? | BLEU/ROUGE | Notes |
|-------|------|--------------|-------------|--------|
| Transformer | Translation | ✔ | High | Stable, accurate output |
| Transformer | Translation | ❌ | Medium | Needs more data |
| GPT | Translation | ✔ | High | More natural phrasing |
| GPT | Scratch | ❌ | Low | Difficult to train fully |
| Transformer/GPT + RL | Summarization | ✔ | Better ROUGE | RL improves summary precision |

---
### Clone the repository
```bash
git clone https://github.com/quocduy1234231/Vietnamese-Text-Summarization-Translation.git
