# Local AI Agent with Ollama and LangChain

A Python-based local AI agent that can answer questions based on CSV data using Retrieval Augmented Generation (RAG). This project uses Ollama for local LLM inference, LangChain for the AI framework, and ChromaDB for vector storage.

## Features

- 100% local execution - no cloud dependencies
- Uses Ollama for local LLM inference
- Vector search capability using ChromaDB
- RAG (Retrieval Augmented Generation) implementation
- Example with restaurant reviews data

## Prerequisites

- Python 3.x installed ([Download Python](https://www.python.org/downloads/))
- Ollama installed ([Download Ollama](https://ollama.com/))

## Installation Steps

1. **Create and activate a virtual environment:**

   Windows:
   ```powershell
   python -m venv venv
   .\venv\Scripts\activate
   ```

   Mac/Linux:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

2. **Install required packages:**
   ```powershell
   pip install -r requirements.txt
   ```
   
   Or install individually:
   ```powershell
   pip install langchain
   pip install langchain-llama
   pip install langchain-chroma
   pip install pandas
   ```

3. **Install Ollama Models:**

   After installing Ollama from [ollama.com](https://ollama.com/), run these commands:
   ```powershell
   ollama pull llama2:3.2
   ollama pull nomic-embed-text
   ```

   To verify installed models:
   ```powershell
   ollama list
   ```

## Project Structure

```
local-ai-agent/
├── main.py              # Main application file
├── vector.py           # Vector store setup
├── requirements.txt    # Python dependencies
└── realistic_restaurant_reviews.csv  # Sample data
```

## Technical Details

- **LLM**: Using Llama 3.2 via Ollama for local inference
- **Embeddings**: nomic-embed-text for document vectorization
- **Vector Store**: ChromaDB for efficient similarity search
- **Framework**: LangChain for AI operations
- **Data Storage**: Local persistent ChromaDB database

## Abbreviations

- **LLM**: Large Language Model
- **RAG**: Retrieval Augmented Generation
- **CSV**: Comma-Separated Values
- **DB**: Database

## Usage

1. Start Ollama service in background
2. Run the application:
   ```powershell
   python main.py
   ```
3. Ask questions about the restaurant reviews
4. Type 'q' to quit

## Example Queries

- "How are the vegan options?"
- "What's the ambiance like?"
- "How is the quality of pizza?"

## Links

- [Ollama Website](https://ollama.com/)
- [Ollama Model Library](https://ollama.com/library)
- [LangChain Documentation](https://python.langchain.com/docs/get_started/introduction.html)
- [ChromaDB Documentation](https://docs.trychroma.com/)

## Note

This project demonstrates how to build an AI agent that runs completely locally without requiring any cloud services or API keys. The example uses restaurant reviews, but you can modify it to work with any type of data by adjusting the document creation process in `vector.py`.