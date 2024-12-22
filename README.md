# -Chat-with-PDF-Using-RAG-Pipeline-
Sithafal Task-1
# PDF Question Answering with LangChain and FAISS

This project demonstrates how to build a simple question-answering system for PDF documents using LangChain, FAISS, and Sentence Transformers.

## Overview

The system works by:

1. **Extracting text from a PDF:** Using PyPDF2, the text content is extracted from the input PDF file.
2. **Chunking the text:** The extracted text is divided into smaller chunks using LangChain's `RecursiveCharacterTextSplitter`.
3. **Generating embeddings:** Sentence Transformers are used to generate embeddings for each text chunk, representing the semantic meaning of the text.
4. **Creating a FAISS index:** The embeddings are stored in a FAISS index for efficient similarity search.
5. **Handling user queries:** When a user enters a query, it is embedded using the same Sentence Transformer model.
6. **Searching the index:** The FAISS index is searched for chunks that are semantically similar to the query.
7. **Generating a response:** The most relevant chunks are used as context for a free LLM (like Flan-T5) to generate a response to the query.

## Requirements

- Python 3.7+
- PyPDF2
- LangChain
- Sentence Transformers
- FAISS
- Transformers
- Pandas

To install these requirements, run:
