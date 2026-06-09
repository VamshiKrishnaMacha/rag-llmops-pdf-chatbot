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

## Author

Vamshi Krishna Macha

