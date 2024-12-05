# PDF Sensei 🥷📚

## Overview

PDF Sensei is a machine learning-powered application that allows users to upload multiple PDF documents and interactively ask questions based on their content. The app processes and extracts information from uploaded PDFs to provide context-aware answers.

## Features

- Upload multiple PDF documents for analysis.
- Automatically extracts and processes text from the PDFs.
- Splits text into manageable chunks for efficient querying.
- Uses advanced language models (**FLAN-T5 Large**) for natural language understanding.
- Employs vector-based semantic search with **Instructor-XL embeddings** for accurate retrieval.
- Maintains conversation history to provide context-aware answers.

## How It Works

1. **PDF Upload**: Users upload one or more PDF files via the app.
2. **Text Extraction**: The app extracts text from all uploaded PDFs using `PyPDF2`.
3. **Chunking**: Text is split into manageable chunks using `CharacterTextSplitter`.
4. **Vectorization**: The chunks are converted into embeddings using **HuggingFace Instructor-XL** and stored in a **FAISS vector database**.
5. **Conversational Chain**: A **Conversational Retrieval Chain** powered by **FLAN-T5 Large** enables users to query the documents conversationally.
6. **Interactive Q&A**: The app dynamically retrieves and answers questions while maintaining conversational context.

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- setup Python virtual environment
  ```bash
  python -m venv venv
  ```
- Point Python to venv that we just created
  ```bash
  source venv/bin/activate
  ```
- Install libraries
  ```bash
  pip install -r requirements.txt
  ```
- Run the application
  ```bash
  streamlit run app.py
  ```

# Architecture

![Architecture Diagram](https://raw.githubusercontent.com/akshaychavan7/PDF-SENSEI/refs/heads/main/assets/PDF%20SENSEI%20Architecture.png)

# Working Demo

<iframe width="560" height="315" src="https://www.youtube.com/embed/0Q2D_QP9nps?si=_0io1Vo4GL7tcNLb" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
