# LLM + RAG-Based Function Execution API

## Overview

This Python-based API service dynamically retrieves and executes automation functions using **LLM (Large Language Models)** combined with **RAG (Retrieval-Augmented Generation)**. The system processes user prompts, maps them to predefined automation functions, and generates executable Python code to invoke those functions.

### Features:
- Execute common automation tasks such as opening applications (e.g., Chrome, Calculator) or retrieving system information (e.g., CPU, RAM usage).
- Use Hugging Face or spaCy models to convert user queries into embeddings.
- Retrieve matching functions dynamically based on the user's input.
- Generate and return executable Python code for the matched function.
- Expose the functionality via a FastAPI service.

## Prerequisites

Before running the application, ensure that you have Python 3.x installed.

### Dependencies:
- **fastapi**: Web framework for building the API.
- **uvicorn**: ASGI server to run the FastAPI app.
- **transformers**: Hugging Face transformers for embedding generation.
- **spacy**: For generating text embeddings using spaCy.
- **sentence-transformers**: For using pre-trained SentenceTransformer models.
- **faiss-cpu**: Vector database for storing and retrieving function embeddings.

To install the required dependencies, create a virtual environment and run the following:
```bash
pip install -r requirements.txt


