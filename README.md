# Legal RAG Pipeline
## Description

- A Retrieval-Augmented Generation (RAG) pipeline for legal documents.
The system retrieves relevant legal text (acts, cases, judgments, contracts) and generates grounded answers using an LLM.

## Features

- Supports large legal documents (PDF, TXT, DOCX)

- Semantic search using vector embeddings

- LLM-based answer generation

- Source-aware responses

- Modular and extensible design

- Scalable for statutes and court judgments

## Architecture

#User Query
→ Embedding Model
→ Vector Database (FAISS)
→ Relevant Legal Chunks
→ LLM
→ Final Answer with Context

## Tech Stack

- Python

- FAISS
  
- OpenAI

- LangChain

## Installation

git clone https://github.com/yourusername/legal_rag_pipeline.git
cd legal_rag_pipeline
pip install -r requirements.txt

## Environment Variables

- Create a .env file:

- OPENAI_API_KEY=your_api_key_here

Add Legal Documents

Build Vector Store
python src/pipeline.py --index


This will:

- Load documents

- Chunk them

- Generate embeddings

- Store them in vector database

Ask Questions
python main.py


## Example:

What is Section 420 IPC?
Explain bail conditions in CrPC.

Example Output
Answer:
Section 420 IPC deals with cheating and dishonestly inducing delivery of property.

Source:
- IPC.pdf (page 112)
- Judgment_2023.pdf (para 4)

## Use Cases

Legal research assistant

Law student study tool

Contract clause analysis

Court judgment summarization

Compliance QA system

## Future Improvements

UI using Streamlit or React

Multi-language support

Case law citation ranking

Hybrid search (BM25 + Vector)

Evaluation using legal QA datasets

## Disclaimer

This project is for educational and research purposes only.
It does not provide legal advice.

## License

MIT License
