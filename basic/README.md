# Basic RAG Project

A simple Retrieval-Augmented Generation (RAG) implementation using transformers, FAISS, and PyTorch.

## Project Structure

```
basic/
├── example.ipynb         # Jupyter notebook with RAG examples
├── pyproject.toml       # Project configuration and dependencies
└── README.md           # This file
```

## Dependencies

- `transformers` - Hugging Face transformers library for models
- `faiss-cpu` - FAISS for efficient similarity search
- `torch` - PyTorch for deep learning
- `scikit-learn` - Machine learning utilities

## Setup

### 1. Initialize the project (already done)
```bash
uv init --name basic-project
```

### 2. Create virtual environment (already done)
```bash
uv venv
```

### 3. Install dependencies (already done)
```bash
uv sync
```

## Usage

### Running with uv
```bash
# Run Jupyter notebook
uv run jupyter notebook

# Interactive Python
uv run python
```

### Running with activated environment
```bash
# Activate virtual environment
source .venv/Scripts/activate  # Windows with Git Bash
# or
.venv\Scripts\activate         # Windows Command Prompt

# Then run normally
python main.py
jupyter notebook
```
### Jupyter Notebook
The notebook `example.ipynb` contains a complete RAG implementation with:
- Document embedding using sentence transformers
- FAISS index for similarity search
- T5 model for text generation
- Example queries and responses

## RAG Implementation Details

The example demonstrates:
1. **Document Embedding**: Using `all-MiniLM-L6-v2` model to create embeddings
2. **Vector Search**: FAISS index for efficient similarity search
3. **Context Retrieval**: Finding most relevant documents for a query
4. **Text Generation**: Using T5 model to generate answers based on retrieved context

## Example Usage

```python
# The notebook contains examples like:
question = "What is the name of the federation that governs the Brazil national football team?"
answer = rag_query(question)
print(answer)
```

## Troubleshooting

### Jupyter not found
If you get "jupyter not found" error, install it:
```bash
uv add jupyter
```

### Model downloads
The first run will download models from Hugging Face. This may take a few minutes depending on your internet connection.

## Next Steps

- Add more documents to the knowledge base
- Experiment with different embedding models
- Try different generation models
- Implement document preprocessing
- Add evaluation metrics
