# Sithafal_task1
Chat with PDF Using RAG Pipeline
This Python script is designed for processing PDF files, creating a searchable knowledge base using vector embeddings, and querying it with natural language questions. It integrates various tools and libraries to streamline the process of text extraction, embedding creation, and question-answering with an AI model. Below is a detailed breakdown of the script:
# 1. Library Imports:

  - pdfminer.high_level.extract_text: Extracts text from PDFs.
  - os and pickle: Handles file operations and serialized data storage.
  - time: Adds delays for better process flow.
  - LangChain Libraries: Facilitates text processing, vector search, and retrieval.
# 2. LLM Initialization:

  - ChatGroq: A robust LLM using the "llama-3.1-70b-versatile" model, accessed via API Key.
# 3. File Upload in Google Colab:

  - google.colab.files: Enables PDF uploads directly in the Colab environment.
# 4. PDF Text Processing:

  - Text Extraction: Extracts PDF text using pdfminer.
  - Text Splitting: Splits text into 1000-character chunks with 100-character overlaps using RecursiveCharacterTextSplitter.
  - Embedding Creation: Generates embeddings using sentence-transformers/all-MiniLM-L6-v2.
  - Vector Store: Stores embeddings in a FAISS index for efficient searches.
  - Pickle Save: Serializes the FAISS index for reuse.
# 5. Query and Retrieval:

  - Users enter queries via input().
  - The FAISS index is loaded with pickle.
  - A RetrievalQA chain enables natural language Q&A using the LLM and indexed data.
# 6. Key Features:

  - Efficient Text Search: Uses FAISS and embeddings for fast similarity-based searches.
  - Interactive Q&A: Provides answers in natural language.
  - Reusable Knowledge Base: Saves processing time by reusing the FAISS index.
  - Scalability: Handles multiple PDFs and large datasets.
# 7. Applications:
  - Creating searchable knowledge bases from documents.
  - Automating text-based Q&A systems.
  - Enhancing productivity in domains like research, legal, and education by providing instant access to relevant information.


This system is ideal for combining document analysis with advanced AI-powered Q&A functionalities.
