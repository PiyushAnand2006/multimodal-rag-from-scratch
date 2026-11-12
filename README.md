# Multimodal RAG from Scratch

This project builds a **multimodal Retrieval-Augmented Generation (RAG) pipeline from scratch** using a research paper PDF.

The pipeline:

1. Extracts text, tables, and images from a PDF using Unstructured.
2. Splits the extracted content into title-aware chunks.
3. Creates searchable summaries for text, tables, and images.
4. Generates embeddings using NVIDIA AI endpoints.
5. Stores the embeddings in ChromaDB for retrieval.

## Project Structure

```text
.
├── Multimodal_RAG.ipynb
├── docs/
│   └── NIPS-2017-attention-is-all-you-need-Paper.pdf
└── README.md
```

## Repository Name

Recommended GitHub repository name:

```text
multimodal-rag-from-scratch
```

## Requirements

- Python 3.10+
- Tesseract OCR
- NVIDIA API key

Install the Python dependencies:

```bash
pip install -U unstructured[all-docs] langchain langchain-community \
    langchain-chroma langchain-nvidia-ai-endpoints python-dotenv \
    pytesseract
```

## Configuration

Create a `.env` file in the project root:

```env
NVIDIA_API_KEY=your_nvidia_api_key
```

Do not commit `.env` or expose your API key publicly.

## Running the Notebook

1. Open `Multimodal_RAG.ipynb`.
2. Select the project virtual environment as the Jupyter kernel.
3. Run the cells from top to bottom.
4. Ensure the PDF path points to the file in `docs/`.

The notebook uses the NVIDIA embedding model:

```python
nvidia/nemotron-3-embed-1b
```

## Status

This is an educational project demonstrating how to create a multimodal RAG system from scratch.
