# Local RAG Product Expert

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/LangChain-RAG-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Ollama-Local%20LLM-black?style=for-the-badge">
  <img src="https://img.shields.io/badge/ChromaDB-Vector%20Store-orange?style=for-the-badge">
</p>

A lightweight, fully local **Retrieval-Augmented Generation (RAG)** application that transforms a dataset of **Test product: (Polaroid camera reviews)** into an interactive AI product expert.

Built using:

* [LangChain](https://www.langchain.com?utm_source=chatgpt.com)
* [Ollama](https://ollama.com?utm_source=chatgpt.com)
* [Chroma DB](https://www.trychroma.com?utm_source=chatgpt.com)

This project runs **100% locally** with:

* No cloud APIs
* No external inference costs
* Persistent vector memory
* Hallucination-resistant retrieval pipeline

---

# 🚀 Features

* 📚 CSV-based product review ingestion
* 🧠 Local embedding generation using `mxbai-embed-large`
* 🔎 Semantic similarity search with Chroma vector database
* 💬 Interactive command-line chatbot
* 🛡️ Strict system prompt guardrails
* ⚡ Fully offline inference using `llama3.2`
* 💾 Persistent vector storage

---

# 📦 Project Structure

```bash
.
├── vector.py
├── main.py
├── Book(Sheet1).csv
└── chroma_db/
```

### `vector.py`

Handles:

* CSV loading
* Text chunk preparation
* Embedding generation
* Chroma DB persistence

### `main.py`

Handles:

* Retriever configuration (`k=5`)
* System prompt engineering
* User query loop
* Response generation using `llama3.2`

### `Book(Sheet1).csv`

Dataset containing:

* Product names
* Ratings
* Review dates
* Written customer reviews

---

# ⚙️ Installation

## 1️⃣ Install Ollama

Download and install:

[Ollama Official Website](https://ollama.com/download?utm_source=chatgpt.com)

Verify installation:

```bash
ollama --version
```

---

# 📥 Pull Required Models

```bash
ollama pull llama3.2
ollama pull mxbai-embed-large
```

---

# 🧩 Install Dependencies

```bash
pip install langchain-ollama langchain-chroma langchain-core pandas
```

---

# ▶️ Run The Project

```bash
python main.py
```

---

# 🛠️ Tech Stack

| Technology        | Purpose               |
| ----------------- | --------------------- |
| Python            | Core application      |
| LangChain         | RAG orchestration     |
| Chroma DB         | Local vector database |
| Ollama            | Local LLM runtime     |
| llama3.2          | Text generation       |
| mxbai-embed-large | Embedding generation  |
| Pandas            | CSV processing        |


If you found this useful, consider giving the repo a ⭐
