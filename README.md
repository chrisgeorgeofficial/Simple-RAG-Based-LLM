# RAG Pipeline with LangChain and Gemini

This project implements a Retrieval-Augmented Generation (RAG) pipeline using LangChain, SentenceTransformers for embeddings, ChromaDB as the vector store, and Google's Gemini LLM for generation. It demonstrates data ingestion, document processing, embedding generation, vector storage, retrieval, and both simple and advanced RAG querying. The example uses a sample resume PDF (CHRIS-GEORGE.pdf) to query details like projects and experiences.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This repository contains a Jupyter Notebook (`document.ipynb`) that builds a complete RAG pipeline from scratch. It starts with loading and processing documents (text files and PDFs), chunks them, generates embeddings, stores them in a vector database, and implements retrieval and generation using an LLM. Advanced features include query history, answer summarization, streaming responses, and citations.

The pipeline is demonstrated by querying details from a sample resume PDF, such as project descriptions.

## Features
- **Document Ingestion**: Load and process text files and PDFs using LangChain loaders (TextLoader, DirectoryLoader, PyMuPDFLoader).
- **Document Splitting**: Chunk documents into manageable sizes with overlap using RecursiveCharacterTextSplitter.
- **Embeddings**: Generate embeddings using SentenceTransformers (`all-MiniLM-L6-v2` model).
- **Vector Store**: Persist embeddings in ChromaDB for efficient similarity search.
- **Retrieval**: Custom retriever class for querying the vector store with score thresholds.
- **Simple RAG**: Basic query-response pipeline using Gemini LLM.
- **Advanced RAG**: Includes streaming answers, citations with sources, query history tracking, and optional summarization.
- **Example Queries**: Querying resume details like "Healthcare Chatbot for Disease Diagnosis and Guidance". ( I used my resume as the datasource )

## Technologies Used
- **Python 3.11+**
- **LangChain**: For document loading, splitting, and RAG components.
- **SentenceTransformers**: For generating embeddings.
- **ChromaDB**: As the vector database.
- **Google Generative AI (Gemini)**: For LLM-based answer generation.
- **Other Libraries**: NumPy, scikit-learn, tqdm, dotenv, etc.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/chrisgeorgeofficial/rag-pipeline-langchain-gemini.git
   cd Simple-RAG-Based-LLM
