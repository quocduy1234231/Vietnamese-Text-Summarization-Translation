# 🧠 Machine Translation & Reinforcement Learning for NLP  
Một dự án cá nhân nghiên cứu về **dịch máy (EN → VI)** và **ứng dụng Reinforcement Learning** trong mô hình ngôn ngữ.

Dự án bao gồm:
- Xây dựng và so sánh các mô hình *Transformer* và *GPT* cho bài toán dịch Anh → Việt.
- Tìm hiểu các thuật toán RL hiện đại như **PPO, TRPO, A2C, SAC** và cách chúng được ứng dụng để tối ưu mô hình ngôn ngữ lớn (LLMs).
- Thực nghiệm, đánh giá, và phân tích kết quả bằng BLEU & ROUGE.

---

## 🚀 Mục tiêu dự án
- Xây dựng pipeline hoàn chỉnh cho bài toán Machine Translation.
- So sánh **pre-trained vs. training-from-scratch** trên cả Transformer và GPT.
- Khám phá vai trò của RL trong tối ưu hóa mô hình sinh văn bản.
- Tối ưu chất lượng dịch qua các kỹ thuật attention và tokenization (BPE).

---

## 📊 Dataset

Dữ liệu của dự án được tổng hợp từ:
- Nguồn song ngữ **OPUS**
- Tập câu bổ sung sinh bằng mô hình Gemini
- Xử lý và chuẩn hóa bằng:
  - Tokenization  
  - Byte Pair Encoding (BPE)  
  - Padding / Truncation  
  - Tách Train – Validation – Test  

Hai tập dữ liệu chính:
en_sents_dataset.txt
vi_sents_dataset.txt
---

## 🏗️ Mô hình được sử dụng

### 🔹 Transformer
- Kiến trúc Encoder–Decoder đầy đủ
- Multi-Head Self-Attention  
- Masked Attention cho Decoder  
- Pre-trained + Fine-tuning  
- Huấn luyện từ đầu (baseline)

### 🔹 GPT (Decoder-only Transformer)
- Masked Multi-Head Attention  
- Dự đoán token tiếp theo (Causal LM)
- GPT-2 Fine-tuning
- GPT training from scratch

---

## 🧪 Thực nghiệm & Kết quả

4 mô hình được huấn luyện và đánh giá:

| Mô hình | BLEU | ROUGE-1 | ROUGE-2 | ROUGE-L | Nhận xét |
|--------|------|----------|----------|-----------|---------|
| **Transformer (Pre-trained)** | Cao nhất | ✔ | ✔ | ✔ | Ổn định, dịch tốt |
| Transformer (Scratch) | Thấp hơn | – | – | – | Cần dữ liệu lớn hơn |
| **GPT (Pre-trained)** | Tốt | ✔ | ✔ | ✔ | Câu dịch mượt và tự nhiên |
| GPT (Scratch) | Thấp | – | – | – | Khó học do dữ liệu hạn chế |

👉 *Mô hình mạnh nhất:* **Transformer Pre-trained** và **GPT Pre-trained**

---

## ⚙️ Cách chạy dự án

### 1️⃣ Clone repo
```bash
git clone https://github.com/quocduy1234231/Vietnamese-Text-Summarization-Translation.git
