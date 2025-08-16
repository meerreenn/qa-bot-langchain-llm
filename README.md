# QA Bot Using LangChain, Watsonx, and RAG

This project implements a **Question Answering (QA) bot** powered by **IBM Watsonx LLM**, **LangChain**, and **Retrieval-Augmented Generation (RAG)**.  
The application allows users to upload a **PDF document** and ask questions. The bot retrieves the most relevant document chunks using embeddings and a vector database, then generates context-aware answers with the LLM.

---

## 🚀 Features
- Upload and process PDF documents.  
- Split text into manageable chunks for efficient retrieval.  
- Generate embeddings using **WatsonxEmbeddings**.  
- Store and retrieve document chunks from a **Chroma vector database**.  
- Use **Watsonx LLM (Mistral model)** for generating natural language answers.  
- Built with **LangChain** for chaining LLM, embeddings, and retriever logic.  
- Clean and interactive **Gradio UI** for easy testing.  

---

## 🧩 Architecture
The pipeline is based on **RAG (Retrieval-Augmented Generation):**

1. **Document Loading** → PDF parsed with `PyPDFLoader`.  
2. **Text Splitting** → Text divided into chunks using `RecursiveCharacterTextSplitter`.  
3. **Embeddings** → Each chunk encoded into vectors using **WatsonxEmbeddings** (`ibm/slate-125m-english-rtrvr`).  
4. **Vector Store** → Chunks stored and indexed in **Chroma**.  
5. **Retriever** → Relevant chunks fetched for a given query.  
6. **LLM Generation** → Query + retrieved context passed to **Watsonx LLM (Mistral)**.  
7. **Answer** → Response displayed in the Gradio interface.  

---

## 📂 Tech Stack
- **Python**  
- **LangChain**  
- **IBM Watsonx (LLM & Embeddings)**  
- **ChromaDB** (Vector Database)  
- **Gradio** (UI)  

## 📚 A View of UI
<img width="1470" height="838" alt="Screenshot 2025-08-16 at 11 55 26" src="https://github.com/user-attachments/assets/2958d8a2-186a-4e95-8120-acd1afb7cca6" />

