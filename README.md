<div align="center">

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=C8A2FF&height=220&section=header&text=ML%20Notes%20PDF%20Chatbot&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=GenAI%20|%20NLP%20|%20FAISS%20|%20Groq%20LLM&descAlignY=58&descColor=ffffff&descSize=18"/>

# 📊 Power BI PDF Chatbot

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![FAISS](https://img.shields.io/badge/FAISS-4285F4?style=for-the-badge)
![Sentence Transformers](https://img.shields.io/badge/Sentence--Transformers-FF6F00?style=for-the-badge)
![Groq](https://img.shields.io/badge/Groq-F55036?style=for-the-badge)

### 🚀 AI-Powered Chatbot to Ask Questions from Power BI PDF Notes

</div>

---

# 📖 Project Overview

The **Power BI PDF Chatbot** is a Retrieval-Augmented Generation (RAG) application that enables users to ask questions about Power BI concepts directly from a PDF document.

Instead of answering from the LLM's general knowledge, the chatbot retrieves the most relevant content from the uploaded Power BI PDF using **semantic search** with **FAISS** and **Sentence Transformers**, then generates accurate responses using **Groq's Llama 3.3 70B** model.

The project demonstrates an end-to-end RAG pipeline including:

- PDF Text Extraction
- NLP Text Preprocessing
- Text Chunking
- Sentence Embeddings
- FAISS Vector Database
- Similarity Search
- Context-aware Answer Generation

---

# 🎯 Objective

Develop an intelligent chatbot capable of answering questions from a Power BI PDF using:

- 📄 PDF Processing
- 🧠 NLP Preprocessing
- 🔍 Semantic Search
- ⚡ FAISS Vector Database
- 🤖 Groq LLM
- 📚 Retrieval-Augmented Generation (RAG)

---

# 📂 Project Structure

```text
PowerBI-PDF-Chatbot/
│
├── power bi.pdf              # Source Power BI PDF
├── stat.ipynb                # Complete chatbot notebook
├── power_index/              # Saved FAISS vector database
├── .env                      # API key
├── requirements.txt
└── README.md
```

---

# 📄 Dataset

The chatbot uses a **Power BI PDF document** as its knowledge source.

Instead of using a structured dataset, every answer is retrieved directly from the uploaded PDF through semantic similarity search.

---

# ⚙️ Complete Workflow

```text
Power BI PDF
      │
      ▼
Extract Text (PyPDF)
      │
      ▼
Text Cleaning
      │
      ▼
Lowercase Conversion
      │
      ▼
Remove HTML
      │
      ▼
Remove Punctuation
      │
      ▼
Remove Numbers
      │
      ▼
Tokenization
      │
      ▼
Stopword Removal
      │
      ▼
Lemmatization
      │
      ▼
Recursive Character Text Splitter
      │
      ▼
Sentence Transformer Embeddings
      │
      ▼
FAISS Vector Database
      │
      ▼
User Question
      │
      ▼
Similarity Search
      │
      ▼
Retrieved Context
      │
      ▼
Groq Llama 3.3 70B
      │
      ▼
Final Answer
```

---

# 🧠 Technologies Used

- Python
- PyPDF
- BeautifulSoup
- NLTK
- LangChain
- RecursiveCharacterTextSplitter
- Sentence Transformers
- HuggingFace Embeddings
- FAISS
- Groq API
- Jupyter Notebook

---

# 🤖 Core Components

## PDF Processing

- PDF Reading
- Text Extraction
- Data Cleaning

## NLP Processing

- Lowercase Conversion
- HTML Removal
- Punctuation Removal
- Number Removal
- Tokenization
- Stopword Removal
- Lemmatization

## Text Chunking

- RecursiveCharacterTextSplitter
- Chunk Size = 500
- Chunk Overlap = 50

## Embedding Generation

Model Used

```
sentence-transformers/all-MiniLM-L6-v2
```

Converts every chunk into dense vector embeddings.

---

# ⚡ Vector Database

The generated embeddings are stored inside **FAISS**, enabling efficient semantic similarity search.

Features:

- Fast Retrieval
- Local Storage
- High-dimensional Vector Search
- Persistent Index

---

# 🤖 LLM Used

Groq API

Model

```
llama-3.3-70b-versatile
```

The LLM receives only the retrieved chunks as context and generates grounded answers.

---

# 📝 NLP Pipeline

- PDF Extraction
- Lowercase
- HTML Removal
- Remove Punctuation
- Remove Numbers
- Tokenization
- Stopword Removal
- Lemmatization
- Text Chunking
- Embedding Generation
- FAISS Storage
- Similarity Search
- LLM Response Generation

---

# 📊 RAG Architecture

```text
Power BI PDF
      │
      ▼
PyPDF
      │
      ▼
NLP Cleaning
      │
      ▼
Chunking
      │
      ▼
Sentence Embeddings
      │
      ▼
FAISS
      │
      ▼
Similarity Search
      │
      ▼
Retrieved Context
      │
      ▼
Groq LLM
      │
      ▼
Answer
```

---

# ✨ Features

- ✅ Power BI PDF Question Answering
- ✅ NLP-based Text Cleaning
- ✅ Semantic Search
- ✅ FAISS Vector Storage
- ✅ Local Vector Database
- ✅ Fast Retrieval
- ✅ Groq LLM Integration
- ✅ Context-aware Responses
- ✅ End-to-End RAG Pipeline

---

# 🚀 Installation

Clone Repository

```bash
git clone https://github.com/your-username/PowerBI-PDF-Chatbot.git
```

Navigate

```bash
cd PowerBI-PDF-Chatbot
```

Install Dependencies

```bash
pip install pypdf
pip install beautifulsoup4
pip install nltk
pip install sentence-transformers
pip install faiss-cpu
pip install langchain
pip install langchain-community
pip install langchain-groq
pip install python-dotenv
```

---

# 🔑 API Setup

Create a `.env`

```text
GROQ_API_KEY=your_api_key
```

Load the API

```python
from dotenv import load_dotenv
import os

load_dotenv()

api_key = os.getenv("GROQ_API_KEY")
```

---

# ▶️ Run Project

```bash
jupyter notebook stat.ipynb
```

Run all notebook cells.

---

# 💬 Example

```python
question = "What is Power BI?"

search = vector_db.similarity_search(question, k=4)
```

Output

```
Power BI is a business intelligence and data visualization platform developed by Microsoft that enables users to connect, transform, analyze, and visualize data using interactive dashboards and reports.
```

---

# 🛠 Skills Demonstrated

- Generative AI
- Retrieval-Augmented Generation (RAG)
- NLP
- LangChain
- Sentence Transformers
- HuggingFace Embeddings
- Vector Databases
- FAISS
- Semantic Search
- Prompt Engineering
- Python
- Groq API

---

# 🔮 Future Improvements

- Streamlit Web Application
- Chat Memory
- Multi-PDF Support
- Source Page References
- Hybrid Search (BM25 + FAISS)
- Docker Deployment
- FastAPI Integration
- Cloud Deployment
- Authentication
- Voice-based Question Answering

---

# 📌 Applications

- Power BI Learning Assistant
- Business Intelligence Tutor
- Technical Documentation Chatbot
- Corporate Knowledge Base
- Interactive Learning Platform
- AI Study Assistant

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to GitHub
5. Create a Pull Request

---

# 👨‍💻 Author

## **Chandru Venkatasamy**

**Data Science | Generative AI | NLP | Machine Learning Enthusiast**

🔹 Passionate about building intelligent AI applications using RAG, LangChain, FAISS, and LLMs.

🔹 Exploring Data Science, Machine Learning, Deep Learning, and Generative AI.

📧 **GitHub:** https://github.com/chandruvenkat-01

---

<div align="center">

## ⭐ If you found this project helpful, consider giving it a Star!

### 💬 "Transforming static Power BI documents into intelligent conversational assistants using RAG."

<img src="https://capsule-render.vercel.app/api?type=waving&color=C8A2FF&height=120&section=footer"/>

</div>