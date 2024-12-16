# Sithafal_task
This script is designed for processing and querying large text data extracted from PDFs or websites using advanced AI models. It employs text embedding and vector search technologies to create a knowledge base for efficient information retrieval. Here's a detailed breakdown:
# Features and Functionality:
  # Task 1: Processing and Querying PDF Files
    - PDF Text Extraction: Extracts text content from PDF files using the pdfminer library.
    - Text Splitting: Divides the extracted text into manageable chunks (1000 characters with a 100-character overlap) for embedding.
    - Vector Embedding Creation: Uses the HuggingFace embedding model (sentence-transformers/all-MiniLM-L6-v2) to convert text chunks into vector embeddings.
    - FAISS Vector Store: Embeds the processed text into a FAISS (Facebook AI Similarity Search) index for efficient similarity-based search.
    - Query Handling: Allows users to input a natural language question. The query is processed by an LLM (ChatGroq) using the FAISS index to retrieve relevant information from the PDF data.
  # Task 2: Web Content Scraping and Querying
    - Web Scraping: Extracts text content from web pages using BeautifulSoup. The script processes all paragraph tags (<p>) to retrieve meaningful information.
    - Embedding and Vector Store:Similar to Task 1, it converts the scraped content into embeddings and stores them in a FAISS index.
    - Query Handling: Enables users to ask natural language questions about the scraped content. The LLM retrieves answers based on the vector similarity from the web data.

# Key Components:
  # Libraries:
    - PDF Processing: pdfminer.six for text extraction.
    - Web Scraping: BeautifulSoup for parsing HTML.
    - AI Processing: langchain, langchain-groq for LLM integration and embedding creation.
    - Vector Search: FAISS for storing and querying embeddings.
 # LLM Integration:
    - The script uses ChatGroq with a temperature setting of 0 for deterministic responses, leveraging the llama-3.1-70b-versatile model for high-quality answers.
 # Reusability:
    - Embedding indexes are stored in a pickle file (faiss_store_openai.pkl), enabling reuse without reprocessing.


# Applications:
    - Building searchable knowledge bases from PDFs or websites.
    - Automating Q&A systems for documents or web content.
    - Enhancing productivity in research, education, or legal workflows by providing instant access to relevant information.

# How It Works:
    - Upload PDFs or Provide URLs: Users can upload PDF files or input website URLs.
    - Processing Text Data: The script extracts, splits, and embeds text data for indexing.
    - Ask Questions: Users can query the processed data to get specific, relevant answers using an advanced AI model.


This script provides a robust framework for leveraging AI in handling and querying complex datasets effectively.
