# fuzzy-bassoon
Implementing a RAG System chatbot for Power BI Usage
# 💡 Power BI RAG Assistant

## 🔍 Overview
**Power BI RAG Assistant** is an AI-powered tool that enables users to query **Power BI documentation** using natural language.  
It combines **retrieval-augmented generation (RAG)** and **LLM-based reasoning** to deliver concise, context-aware answers, helping analysts navigate complex documentation efficiently.

---

## 🧠 What It Does
- Converts Power BI PDFs into searchable embeddings using **LangChain** and **OpenAI Embeddings**  
- Stores them in **ChromaDB** with an **HNSW (cosine similarity)** index for fast retrieval  
- Uses **GPT-4o-mini** to generate clear, contextual answers  
- Includes a **Gradio interface** for interactive chat-style queries  

---

## ⚙️ Tech Stack
| Component | Tool |
|------------|------|
| Vector DB | ChromaDB (HNSW Index) |
| LLM | OpenAI GPT-4o-mini |
| Embeddings | text-embedding-3-small |
| Framework | LangChain |
| UI | Gradio / Streamlit |
| Environment | Google Colab |

---

## 🚀 Key Highlights
✅ End-to-end RAG pipeline (PDF → Embeddings → Retrieval → Response)  
✅ Efficient batch ingestion with persistence and telemetry disabled  
✅ HNSW-based similarity retrieval in cosine space  
✅ Supports both programmatic and UI interaction  
✅ Clean code with inline documentation and markdown insights  

---

## 📊 Example Query
**User:** “What is Power BI?”  
**System:** Retrieves the top 5 most relevant document chunks and generates a concise summary based on context.

---

## 💼 Business Value
This project demonstrates how **AI-assisted document understanding** can:
- Reduce analyst onboarding time  
- Improve tool adoption and data literacy  
- Enable faster, self-service insights across organizations  

---

## 🏁 Run It Locally
```bash
pip install langchain langchain-openai langchain-chroma chromadb openai gradio
export OPENAI_API_KEY="sk-..."
python rag_gradio.py
