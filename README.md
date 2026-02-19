##Setup Instructions

##Clone the repository

git clone <https://github.com/1sourabhh/RAG-NEURA-DYNAMICS->
cd RAG-NEURA-DYNAMICS-

##Create and activate a virtual environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate


##Install required dependencies
pip install -r requirements.txt


#Configure environment variables
Create a .env file if required

Add model paths, API keys, or configuration details

##Run the application
streamlit run app.py

##Architecture Overview
The system is designed as a modular Generative AI application with agent-based orchestration.
Frontend: Streamlit for interactive chat UI
LLM Layer: Local or hosted LLM for response generation
Prompt Management: MCP for managing prompts, memory, and context
Agent Orchestration: LangGraph for controlling multi-step agent workflows
Retrieval Layer: RAG pipeline for context-aware responses
Vector Database: FAISS / ChromaDB for semantic document retrieval
Embeddings: HuggingFace Embeddings for vector generation
Flow:User Query → Retriever → Context Injection (MCP) → Agent Decision (LangGraph) → LLM → Final Response

##Prompt(s) Used
System Prompt
You are an AI assistant designed to answer user queries accurately
using the provided context. Use retrieved documents, memory,
and instructions to generate clear, concise, and helpful responses.
