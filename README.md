# LLM Fundamentals with OpenAI & Hugging Face Transformers

This repository demonstrates hands-on experimentation with modern Large Language Models (LLMs), combining OpenAI’s GPT models with Hugging Face Transformers.  
The project focuses on understanding **how LLMs work under the hood**, not just calling high-level APIs.

It covers text generation, prompt design, tokenization, transformer pipelines, PyTorch-based inference, and model persistence.

---

## What This Project Covers

### 1. OpenAI GPT (Chat Completions API)
- Text generation with temperature and token control
- Prompt-based customization
- Few-shot prompting patterns
- Task-specific behaviors using system instructions

**Examples**
- Story generation
- Controlled creativity (temperature tuning)
- Keyword extraction (summarization-style task)
- Poetic-style conversational assistant

---

### 2. Hugging Face Transformers Pipelines
Using high-level pipelines to rapidly apply pretrained models:

- **Sentiment Analysis**
- **Named Entity Recognition (NER)**
- **Zero-Shot Classification**

These examples demonstrate how pretrained models can be used *without additional training* for real-world NLP tasks.

---

### 3. Tokenization (Deep Dive)
Exploration of **pre-trained tokenizers** and how different models process text:

- BERT (`bert-base-uncased`)
- XLNet (`xlnet-base-cased`)

Topics covered:
- Token vs token ID
- Vocabulary mappings
- Special tokens (`[CLS]`, `[SEP]`)
- Model-specific tokenization strategies

This section emphasizes why **tokenization must match the model architecture**.

---

### 4. Hugging Face + PyTorch Inference
Manual inference workflow using PyTorch:

- Loading tokenizer and model explicitly
- Converting inputs to tensors
- Running inference with `torch.no_grad()`
- Interpreting logits and predicted labels

This mirrors what Hugging Face pipelines do internally, providing transparency and flexibility for production workflows.

---

### 5. Saving and Loading Models
Demonstrates model persistence for reuse and deployment:

- Saving tokenizer and model locally
- Reloading from disk using `from_pretrained`
- Understanding the role of `config.json`, model weights, and tokenizer assets

This is a key step toward **production-ready ML workflows**.

---

## Key Learning Outcomes

- Understand how LLM APIs differ from transformer-based local inference
- Learn when to use high-level pipelines vs low-level model control
- Gain intuition for tokenization, embeddings, and special tokens
- See how research-style notebooks translate to production practices
- Build a solid mental model of the modern NLP stack

---

## Tech Stack

- **OpenAI API** (GPT-4o-mini)
- **Hugging Face Transformers**
- **PyTorch**
- **Python**
- **dotenv** for environment configuration

---

## Project Structure

```text
.
├── notebooks / scripts
│   ├── openai_text_generation.py
│   ├── summarization_keywords.py
│   ├── poetic_chatbot.py
│   ├── hf_pipelines.py
│   ├── tokenization_exploration.py
│   ├── pytorch_inference.py
│   └── save_load_models.py
├── my_save_models/
│   ├── config.json
│   ├── pytorch_model.bin
│   ├── tokenizer.json
│   └── vocab files
├── .env.example
└── README.md
