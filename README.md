# Abstractive Text Summarization using BART on BillSum

This project applies the **facebook/bart-base** model to the task of abstractive summarization using the BillSum dataset. It includes dataset preparation, model fine-tuning, and evaluation with standard metrics.

## 📜 Dataset

- **BillSum:** U.S. Congressional bills and their human-written summaries
- Provided by Hugging Face `datasets` library

## 🔧 Preprocessing

- Load `text` and `summary` fields
- Tokenize with BART tokenizer
- Truncate/pad to 1024 tokens (input) and 256 tokens (output)
- Use Hugging Face’s `DataCollatorForSeq2Seq` to dynamically pad inputs

## 🧠 Model

- **Base Model:** `facebook/bart-base` (pretrained)
- Fine-tuned using `Seq2SeqTrainer`
- Supports full encoder-decoder summarization

## 🧪 Evaluation Metrics

- ROUGE-L
- SacreBLEU
- BERTScore

These are computed using Hugging Face `evaluate` library.

## 📈 Visuals

- Training and validation loss over epochs
- Sample generated summaries vs. ground truth

## 🧰 Requirements

```bash
pip install datasets transformers evaluate sacrebleu bert_score rouge-score
