# This project involves the following techstack:

1. Streamlit: For frontend

2. FastAPI and Uvicorn: For backend

3. Gemini 1.5 Flash: For agent and RAG implementation

4. langchain: For retriever initialization

5. HuggingFace embeddings: For creating embeddings for vectorDB

6. requests: For making requests to the FastAPI endpoint

7. bm25 retriever: For sparse retrieval

8. tf-idf retriever: For sparse retrieval

9. faiss: for dense retrieval (vectorDB)

10. ensemble retriever: for hybrid retrieval

11. sarvam api endpoint: for Text to Speech

# Steps to replicate this on a local machine

1. Download the repo on your Machine.

2. Install the requirements.txt file using pip install -r requirements.txt.
   
3. Save the SARVAM_API_KEY and GOOGLE_API_KEY in the environment .env file.

4. Enter the file location of the pdf file in file_path variable in the initialize_multiple_retrievers.py file first and run the file using python initialize_multiple_retrievers.py.

5. Use tmux to run 3 different terminals on a single or on vscode open 3 different shells to run the following commands

6. Type uvicorn rag_api_endpoint:app --reload --port 8000 on the first terminal and press Enter

7. Type uvicorn agent_api_endpoint:app --reload --port 8001 on the second terminal and press Enter

8. Type streamlit run front_end.py --port 8501 on the third terminal and press Enter

9. Open the http://localhost:8501/ on your browser and you should be able to utilize the application.
