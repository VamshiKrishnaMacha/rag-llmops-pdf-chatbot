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

<p align="center">
  <img src="screenshots/architecture.png" alt="RAG Chatbot Architecture" width="1000"/>
</p>

### Project Workflow

1. Load PDF using PyPDFLoader
2. Split document into chunks using CharacterTextSplitter
3. Generate embeddings using HuggingFace BGE
4. Store embeddings in Chroma Vector Database
5. User asks a question through Gradio/Streamlit
6. Question is converted into embeddings
7. Similarity search is performed in ChromaDB
8. Relevant chunks are retrieved
9. Context and question are sent to Groq Llama 3.3
10. LLM generates a contextual response
11. LangSmith tracks retrieval, prompts, LLM calls, latency, and responses

```mermaid
flowchart TD

    A[PDF Document<br>Python Built-In Functions.pdf]
    B[PyPDFLoader]
    C[LangChain Documents]
    D[CharacterTextSplitter]
    E[Text Chunks]
    F[HuggingFace BGE Embeddings]
    G[Vector Embeddings]
    H[Chroma Vector Database]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H

    I[User]
    J[Gradio / Streamlit Frontend]
    K[User Question]
    L[Question Embedding]
    M[Similarity Search]
    N[Retrieve Relevant Chunks]
    O[Prompt Construction]
    P[Groq Llama 3.3 LLM]
    Q[Generated Response]

    I --> J
    J --> K
    K --> L
    L --> M
    H --> M
    M --> N
    N --> O
    O --> P
    P --> Q
    Q --> J
    J --> I

    R[LangSmith Tracking]
    S[Monitor Retrieval]
    T[Monitor Prompts]
    U[Monitor LLM Calls]
    V[Monitor Response Time]

    N --> R
    O --> R
    P --> R

    R --> S
    R --> T
    R --> U
    R --> V
```



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

