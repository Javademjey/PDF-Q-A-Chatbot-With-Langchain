# PDF-Q-A-Chatbot-With-Langchain
LangChain-based PDF Q&amp;A Chatbot: parse and chunk PDF content, generate semantic embeddings (OpenAI/HuggingFace) stored in a Chroma vector store, and answer queries with GPT-4o or Llama3 via a Gradio interface.


# 📘 PDF Q\&A Chatbot with Memory

This repository contains a chatbot that lets you ask questions about a PDF file (e.g., Monopoly rulebook) using LangChain, OpenAI, HuggingFace embeddings, and Gradio.
The chatbot supports conversation memory and can run on either:

* 🧠 Llama3-8b (via Ollama, local model)
* 🤖 GPT-4o-mini (via OpenAI API)

---

## ✨ Features

* 📄 PDF Loader → Extracts text from a PDF.
* ✂️ Text Splitter → Breaks text into chunks for better embeddings.
* 🧩 Embeddings → Supports OpenAI and HuggingFace.
* 💾 Vector Database (Chroma) → Stores embeddings for fast retrieval.
* 🗨 Conversational Memory → Chat remembers previous context.
* 🌐 Gradio Web UI → Easy-to-use browser-based chatbot interface.

---

## 🛠 Installation

### 1. Clone Repository

git clone https://github.com/your-username/PDF-Q-A-Chatbot-With-Langchain.git
cd PDF-Q-A-Chatbot-With-Langchain

### 2. Create Virtual Environment

python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

### 3. Install Dependencies

pip install -r requirements.txt

Dependencies include:

* langchain
* langchain-community
* langchain-openai
* langchain-chroma
* sentence-transformers
* gradio
* ollama (if using local Llama3)

### 4. API Keys

* If using OpenAI:
  Edit the code and replace OPENAI_API_KEY = "sk-..." with your actual key.

* If using Llama3 via Ollama:
  Install [Ollama](https://ollama.ai) and pull the model:

    ollama run llama3.1:8b
  

---

## ▶️ Running the Chatbot

1. Place your PDF file in the project directory (e.g., monopoly.pdf).
2. Run the app:

      python app.py
   
3. The Gradio interface will open in your browser automatically.

---

## 💬 Usage

1. Select your model (Llama3-8b or GPT-4o-mini).
2. Type a question related to your PDF (e.g., "What are the rules for buying houses?").
3. The chatbot retrieves relevant PDF chunks + answers with context.
4. Continue chatting — the bot remembers history.

---

## 🧱 Project Structure

PDF-Q-A-Chatbot-With-Langchain/
│── app.py              # Main application
│── monopoly.pdf        # Example PDF (replace with your own)
│── requirements.txt    # Python dependencies
│── README.md           # Documentation
│── vector_db/          # Vector database (auto-generated)

---

## 🧩 Tech Stack

* LangChain → Orchestration & Retrieval
* Chroma → Vector store
* OpenAI API → GPT-4o-mini (optional)
* HuggingFace Embeddings → sentence-transformers/all-MiniLM-L6-v2
* Ollama → Local Llama3 model
* Gradio → Chat UI

---

## 🚀 Future Improvements

* 🔎 Support for multiple PDFs
* 📚 Upload new PDFs via UI
* 🖼 Extract text from scanned PDFs (OCR)
* 🧠 Add summarization mode
  
