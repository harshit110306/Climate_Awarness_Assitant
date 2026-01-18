# 🌍 Climate Awareness RAG Chatbot (Demo Project)

## 📌 Project Overview

The **Climate Awareness RAG Chatbot** is a **demonstration project** that showcases how **Artificial Intelligence (AI)** can be used to improve **climate change awareness** by providing users with **accurate, context-based answers** grounded in trusted documents.

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline using **local resources only**, ensuring:

* No dependency on paid APIs
* No rate limits or quota issues
* Full control over data and models

> ⚠️ **Important Note:**
> This project is built **for demonstration and learning purposes only**.
> It is **not a production-ready system** and does not cover aspects such as large-scale deployment, continuous data updates, authentication, or advanced monitoring.

---

## 🎯 Project Objectives

* Demonstrate the working of **Retrieval-Augmented Generation (RAG)**
* Show how AI can assist in **climate education and sustainability awareness**
* Build a **fully local, cost-free AI chatbot**
* Create a **portfolio-ready project** suitable for academic evaluation and GitHub showcase

---

## 🌱 SDG Alignment

* **Primary SDG:** SDG 13 – Climate Action
* **Secondary SDGs:**

  * SDG 11 – Sustainable Cities and Communities
  * SDG 12 – Responsible Consumption and Production

---

## 🧠 Key Concept: What is RAG?

Retrieval-Augmented Generation (RAG) combines:

1. **Information Retrieval** – Fetching relevant content from documents
2. **Text Generation** – Using an LLM to generate answers grounded in retrieved content

This approach reduces hallucinations and improves answer reliability.

---

## 🏗️ Project Architecture (High Level)

```
User Query
   ↓
Document Retrieval (FAISS Vector DB)
   ↓
Relevant Climate Content
   ↓
Prompt Construction
   ↓
Local LLM (Ollama)
   ↓
Final Answer
```

---

## 🧰 Technologies Used

| Component            | Technology                            |
| -------------------- | ------------------------------------- |
| Programming Language | Python                                |
| Vector Database      | FAISS                                 |
| Embeddings           | Sentence Transformers (HuggingFace)   |
| LLM                  | LLaMA 3.2 / Mistral (via Ollama)      |
| UI                   | Streamlit                             |
| Framework            | LangChain (modular, chain-free usage) |

---

## 📂 Project Structure

```
Climate_chatbot/
│
├── app.py               # Streamlit web application (main interface)
├── ingest.py            # Builds vector database (run once)
├── data/
│   └── climate_docs.txt # Climate knowledge source
├── faiss_db/            # Auto-generated vector store
├── requirements.txt     # Dependencies
└── README.md            # Project documentation
```

---

## 🔄 How the Project Works (Step-by-Step)

### 1️⃣ Data Preparation

A small set of climate-related information is stored in a text file:

```
data/climate_docs.txt
```

This file represents **trusted knowledge** used by the chatbot.

---

### 2️⃣ Document Processing & Embedding

The `ingest.py` script:

* Loads climate documents
* Splits them into smaller chunks
* Converts text into numerical vectors using **sentence-transformer embeddings**
* Stores embeddings in a **FAISS vector database**

This step is executed **only once**.

```bash
python ingest.py
```

---

### 3️⃣ Query Handling

When a user asks a question:

* The query is converted into a vector
* FAISS retrieves the **most relevant document chunks**
* These chunks are used as **context** for the LLM

---

### 4️⃣ Answer Generation

A **local Large Language Model (LLM)** running via **Ollama**:

* Receives the user question
* Receives retrieved context
* Generates a **clear, grounded response**

No internet or paid API is required.

---

### 5️⃣ User Interface

The chatbot is accessed via a **Streamlit web interface**:

* Simple text input
* Real-time responses
* Suitable for demos and presentations

Run the app:

```bash
streamlit run app.py
```

---

## 🤖 Models Used (Local)

* **llama3.2:latest** – Fast, efficient, recommended
* **mistral:latest** – More detailed responses (optional)

Models are managed locally using Ollama:

```bash
ollama list
```
* Used the llama3.2 for this project
---

## ⚖️ Responsible AI Considerations

* No personal data is collected
* All responses are grounded in provided documents
* The system avoids generating speculative or harmful advice
* Designed strictly for educational and awareness purposes

---

## 🚧 Project Limitations (Important)

This project is **NOT fully completed or production-ready**. Limitations include:

* Static knowledge base (manual updates required)
* No real-time climate data integration
* No user authentication
* No scalability or cloud deployment
* No automated evaluation of response quality

These limitations are **intentional**, as the goal is to **demonstrate core RAG concepts**, not build a full product.

---

## 🧪 Intended Use

✔ Academic demos
✔ Internship / SkillsBuild submissions
✔ Portfolio & GitHub showcase
✔ Learning RAG architecture

❌ Not intended for real-world decision-making
❌ Not suitable for policy or medical advice

---

## 🚀 Future Enhancements (Out of Scope for Demo)

* PDF upload & dynamic document ingestion
* Source citations in responses
* Cloud deployment
* Real-time climate APIs
* User feedback loop
* Multi-language support

---

## 👤 Author

**Harshit Bodala**
AI / ML & Data Science Enthusiast

---

## 📜 License

This project is released for **educational and demonstration purposes only**.

---

### ✅ Final Note

This repository demonstrates **how AI can be responsibly applied to sustainability challenges** using modern RAG techniques, while remaining **cost-free, transparent, and easy to understand**.


Just tell me 👍
