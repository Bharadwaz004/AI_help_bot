# 🧠 AI Help Bot – Multi-Agent Document Retrieval, Summarization & Q/A

## 📌 Overview
**Help Bot** is a single-notebook pipeline that:
1. **Retrieves** relevant documents from a ChromaDB vector store.
2. **Summarizes** the retrieved content.
3. **Answers** user questions based on the summary.

It combines:
- **[LangChain](https://www.langchain.com/)** for document loading, splitting, and retrieval.
- **[HuggingFace Transformers](https://huggingface.co/transformers/)** for summarization and Q/A.
- **[Chroma](https://www.trychroma.com/)** for vector database storage.

## 🛠 Features
- **Offline or Online Models**: Can use local models like `t5-base` or API-based models from HuggingFace Hub.
- **Vector-based Search**: Uses ChromaDB for efficient similarity search.
- **End-to-End Notebook**: Everything is in one `.ipynb` for simplicity.
- **Customizable**: Easily replace models or tweak chunk sizes.

## 🚀 How to Run

### Step 1: Upload Your Data
Place all `.txt` documents in the `data/` folder.

### Step 2: Ingest Data into Vector DB
Open and run: ingest_data.ipynb  
This will:
- Load all `.txt` files from `data/`
- Split them into smaller chunks
- Store embeddings in `chroma_db/`

### Step 3: Run the Full Pipeline
Open and run: agents/pipeline.ipynb  
This will:
- Retrieve relevant documents.
- Summarize them using the LLM.
- Answer your question based on the summary.



