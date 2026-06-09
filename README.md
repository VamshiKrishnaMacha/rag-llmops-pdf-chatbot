# rag-llmops-pdf-chatbot
RAG-based PDF Chatbot built using LangChain, ChromaDB, Hugging Face Embeddings, Groq Llama 3.3, LangSmith Tracing, and Gradio. The system performs document ingestion, chunking, vector embedding generation, similarity search, and contextual question answering over PDF documents while providing observability through LangSmith.


# RAG PDF Chatbot with LLMOps
## Gradio Chatbot Interface

![Gradio Chatbot](screenshots/RAG_PDF_ChatBot.png)

## LangSmith Tracing

![LangSmith Tracing](screenshots/Tracing.png)


## Project Overview

This project implements a Retrieval-Augmented Generation (RAG) chatbot that answers questions from PDF documents using LangChain, ChromaDB, Hugging Face Embeddings, Groq Llama 3.3, LangSmith, and Gradio.

## Features

* PDF Document Loading
* Text Chunking
* Vector Embeddings
* ChromaDB Vector Database
* Similarity Search
* RetrievalQA
* Groq LLM Integration
* LangSmith Tracing
* Gradio Chatbot Interface

## Architecture

PDF Document
↓
PyPDFLoader
↓
Text Splitter
↓
Embedding Model
↓
ChromaDB

User Question
↓
Retriever
↓
Relevant Chunks
↓
Groq LLM
↓
Final Response

## Technologies Used

* Python
* LangChain
* ChromaDB
* Hugging Face Embeddings
* Groq Llama 3.3
* LangSmith
* Gradio

## Project Structure

* Notebook: RAG_integration_with_llmops.ipynb
* Dependencies: requirements.txt
* Documentation: README.md

# RAG Chatbot with LangChain, ChromaDB, Groq & LangSmith

## Architecture

### Document Ingestion Phase (One-Time Process)

PDF Document
(Python Built-In Functions.pdf)
        ↓
PyPDFLoader
        ↓
Load PDF into LangChain Documents
        ↓
CharacterTextSplitter
        ↓
Create Chunks
(chunk_size=2000, chunk_overlap=400)
        ↓
HuggingFace BGE Embedding Model
        ↓
Convert Chunks into Embeddings (Vectors)
        ↓
Chroma Vector Database
        ↓
Store Vector Embeddings


### User Query Phase

User
        ↓
Frontend (Gradio / Streamlit)
        ↓
User Question
        ↓
LangChain
        ↓
HuggingFace BGE Embedding Model
        ↓
Convert Question into Embedding
        ↓
Chroma Vector Database
        ↓
Similarity Search
        ↓
Retrieve Most Relevant Chunks
        ↓
LangChain Prompt Template
        ↓
Groq Llama 3.3 LLM
        ↓
Generate Context-Aware Response
        ↓
Frontend
        ↓
User


### LLMOps & Monitoring Phase

User Query
        ↓
Retriever
        ↓
Retrieved Chunks
        ↓
Prompt Creation
        ↓
Groq LLM Response
        ↓
Execution Metrics
        ↓
LangSmith Tracking
        ↓
Monitoring, Debugging & Observability


## End-to-End Workflow

PDF
        ↓
PyPDFLoader
        ↓
Text Extraction
        ↓
Chunking
        ↓
Embeddings
        ↓
Chroma Vector Database

====================================================

User Question
        ↓
Frontend
        ↓
LangChain
        ↓
Question Embedding
        ↓
Vector Search
        ↓
Retrieve Relevant Chunks
        ↓
Groq LLM
        ↓
Generate Answer
        ↓
Frontend
        ↓
User

====================================================

LangSmith
        ↓
Track Retrieval
        ↓
Track Prompt
        ↓
Track LLM Calls
        ↓
Track Response Time
        ↓
Monitor Entire RAG Pipeline


## Tech Stack

- LangChain
- ChromaDB
- HuggingFace BGE Embeddings
- Groq (Llama 3.3 70B)
- LangSmith
- PyPDFLoader
- CharacterTextSplitter
- Gradio / Streamlit
- Python

## Project Type

Retrieval-Augmented Generation (RAG) Chatbot with LLMOps Monitoring

## Author

Vamshi Krishna Macha

