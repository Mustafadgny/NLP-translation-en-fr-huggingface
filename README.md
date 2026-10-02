# 🌐 Neural Machine Translation (NMT) with MarianMT

This repository provides a lightweight implementation of Neural Machine Translation (NMT) using Hugging Face's `transformers` library and the pre-trained `Helsinki-NLP/opus-mt-en-fr` model to translate text from English to French.

## 🚀 Overview

The project demonstrates how sequence-to-sequence transformer architectures handle cross-lingual translation. It tokenizes source sequences, runs autoregressive generation with the translation model, and decodes the resulting token IDs into target language text.

## 🧠 Translation Workflow

1. Model Selection: Uses Helsinki-NLP's MarianMT (`opus-mt-en-fr`), an open-source seq2seq model fine-tuned for English-to-French translation.
2. Tokenization: Encodes raw text into PyTorch tensors with automatic padding using MarianTokenizer.
3. Text Generation: Executes model.generate() to perform autoregressive sequence-to-sequence translation.
4. Decoding: Translates generated token IDs back to human-readable strings while omitting special control tokens (skip_special_tokens=True).

## 🛠️ Tech Stack
- Python
- PyTorch
- Hugging Face Transformers (MarianMT)
- SentencePiece

## 💻 Installation & Usage

1. Install dependencies:
pip install torch transformers sentencepiece

2. Run the translation script:
python machine_translation.py

## 📊 Example Output

- Input (English): "Hello, what is your name"
- Translated Output (French): "Bonjour, quel est votre nom"
