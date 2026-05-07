# 📄 Enterprise RAG Assistant

An end-to-end Retrieval-Augmented Generation (RAG) application that allows users to upload PDF documents and dynamically query their contents using natural language. 

Built with the modern LangChain architecture, this project demonstrates production-grade document ingestion, vector embeddings, and context-aware LLM querying through a clean web interface.

## 🚀 Features

* **Intelligent Document Processing:** Ingests PDFs and intelligently chunks text using `RecursiveCharacterTextSplitter` to maintain semantic meaning.
* **Vector Search:** Utilizes `text-embedding-3-small` and **ChromaDB** for fast, high-dimensional similarity search.
* **Context-Aware Q&A:** Routes retrieved document chunks into a custom system prompt, forcing the LLM (`gpt-4o-mini`) to answer strictly based on the provided context.
* **Modern UI:** Built with **Gradio** for a seamless, interactive chat experience.
* **Fail-Fast Architecture:** Includes built-in error handling, type hinting, and professional logging.

## 🛠️ Tech Stack

* **Language:** Python 3.10+
* **LLM Orchestration:** LangChain (Core, Community, Classic)
* **Embedding & Generation:** OpenAI API (`gpt-4o-mini`, `text-embedding-3-small`)
* **Vector Database:** Chroma
* **Frontend:** Gradio

## ⚙️ Installation & Setup

This application is optimized to run in Google Colab or any standard Python virtual environment.

### 1. Install Dependencies
Run the following command to install the required modern LangChain packages and UI dependencies. The `--no-cache-dir -U` flags ensure you get the latest, uncorrupted architecture:
```bash
pip install --no-cache-dir -U langchain langchain-classic langchain-core langchain-community langchain-text-splitters langchain-openai langchain-chroma pypdf gradio
