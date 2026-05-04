#  PDF RAG Chatbot (LangChain, Gemini, Streamlit)

A production-ready Retrieval Augmented Generation (RAG) chatbot that answers questions using one or more PDF documents as knowledge sources.  
Built using LangChain, Google Gemini, FAISS, and Streamlit, this project enables accurate, context-aware question answering from user-uploaded PDFs.

---

#  Overview

The PDF RAG Chatbot is an AI-powered application that allows users to interact with PDF documents using natural language queries. It leverages Retrieval-Augmented Generation (RAG) to extract relevant information from uploaded PDFs and generate accurate, context-based responses. By combining embeddings, vector search, and a language model, the system provides efficient and reliable document-based question answering with conversational support.

---

#  Problem Statement

Enterprises store large amounts of information in PDF documents, but extracting relevant answers manually is time-consuming and inefficient.  
This project develops a RAG-based chatbot to retrieve and generate accurate answers from PDFs, improving accessibility and productivity.

---

#  Objectives

- To build a chatbot that can answer questions based on PDF content using RAG architecture  
- To improve accuracy using embeddings, vector search, and LLMs  
- To provide an interactive interface for document upload and conversational querying  

---

#  Features

- PDF Extraction  
  - Upload and process multiple PDF files  
  - Extract text using PyPDF2  

- Text Chunking  
  - Splits documents into manageable chunks  
  - Uses RecursiveCharacterTextSplitter with configurable size and overlap  

- Embeddings & Vector Store  
  - Converts text into embeddings using Sentence Transformers  
  - Stores vectors in FAISS for efficient retrieval  

- Semantic Search  
  - Retrieves top-k relevant chunks based on query similarity  

- Conversational Memory  
  - Maintains chat history for multi-turn conversations  
  - Uses LangChain's ConversationBufferMemory  

- LLM Integration  
  - Generates answers using Google Gemini  
  - Integrated via LangChain  

- Streamlit UI  
  - Simple and interactive user interface  
  - Supports PDF upload, chat, and history view  

- Dynamic Configuration  
  - Configurable via `.env` and `src/config.py`  
  - Supports API keys, model settings, chunk size, etc.  

- Error Handling  
  - Robust error handling and retry mechanisms  

- Multi-PDF Filtering  
  - Allows users to select and query a specific PDF  
  - Improves accuracy by restricting search scope  

- Response Download   
  - Download chatbot responses as TXT or PDF  
  - Useful for saving results and documentation  

- Improved User Experience  
  - Displays uploaded file names  
  - Provides better interaction control  

---

#  Tech Stack

- Python  
- LangChain  
- Google Gemini (LLM)  
- FAISS (Vector Database)  
- Sentence Transformers (Embeddings)  
- Streamlit (Frontend UI)  

---

#  Advantages

- Provides accurate answers based on document content (reduces hallucination)  
- Saves time by automating manual document search  
- Supports multiple PDFs and large documents  
- Maintains conversational context for better user experience  
- Can be customized and deployed for enterprise use  
- Enables document-level filtering for precise queries  
- Allows downloading responses for better usability  

---

#  Setup Instructions

1. Clone the Repository  

2. Create Virtual Environment  
   python -m venv venv  

3. Activate Environment  
   venv\Scripts\activate  

4. Install Dependencies  
   pip install -r requirements.txt  

5. Configure Environment Variables  
   Create a .env file in the root directory:  
   GEMINI_API_KEY=your-gemini-api-key-here  

6. Run the Application  
   streamlit run app.py  

---

#  Usage

- Upload one or more PDF files from the sidebar  
- View uploaded file names  
- Click "Process Documents" to extract and embed text  
- Select a specific PDF (optional) to filter search  
- Ask questions in the chat input  
- The chatbot responds based on PDF content  
- Download responses as TXT or PDF  
- Chat history is maintained for context  
- Use "Clear Conversation" to reset  

---

#  Future Improvements
  
- Voice-based interaction  
- Deployment on cloud (AWS/GCP)  
- Offline LLM integration  
- Export full chat history with sources  
- Enhanced document highlighting and visualization  

---

#  Conclusion

The PDF RAG Chatbot demonstrates how Retrieval-Augmented Generation can be effectively used to transform static PDF documents into interactive knowledge systems. By combining document processing, embeddings, vector search, and LLMs, the project delivers accurate and context-aware answers while reducing manual effort. This solution highlights the practical use of modern AI techniques in real-world applications and can be further extended for enterprise-level deployment with enhanced features and scalability.