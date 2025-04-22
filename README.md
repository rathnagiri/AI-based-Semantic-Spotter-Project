# AI-based-Semantic-Spotter-Project
Semantic Spotter - Build a RAG System

## Problem Statement

The goal of this project is to build a robust generative search system capable of effectively and accurately answering questions from various insurance policy documents. This problem falls under the domain of Retrieval Augmented Generation (RAG), where we aim to leverage external knowledge sources (insurance documents) to enhance the capabilities of a language model.

## Solution Overview

The solution utilizes `llamaindex`, a powerful Python library for building RAG systems. `llamaindex` offers a framework for indexing, querying, and retrieving information from documents, enabling efficient and accurate information retrieval.

## Architecture

The architecture of the RAG system consists of the following components:

1.  **Document Indexing:** The insurance policy documents are indexed using `llamaindex` to create a searchable knowledge base. This step involves converting the documents into a structured format suitable for querying.
2.  **Question Processing:** User questions are preprocessed and converted into a format compatible with the indexing mechanism. This step involves text cleaning and potentially transforming the question into a query vector.
3.  **Retrieval:** Relevant information is retrieved from the indexed documents based on the user's question. `llamaindex`'s retrieval module is used to identify the most relevant passages or sections of the documents, potentially utilizing a vector database for similarity search. By default, LlamaIndex uses an in-memory vector store and is utilised here, but can be extended to explicityly configure a third-party vector database like chroma, pinecone, Weaviate, FAISS etc.,
4.  **Generation:** The retrieved information and the user's question are provided as input to a language model, which generates a comprehensive answer. This step involves using the language model to synthesize the retrieved information and formulate a coherent response.


## Dataset Used

The dataset used in this project consists of various insurance policy documents. These documents provide the knowledge base for the RAG system, allowing it to answer questions based on the information contained within the documents. The specific policy documents used can be found in the `data` folder.

## Requirements

To run this project, you need to have the following installed:

*   Python 3.7 or higher
*   OPENAI_API_Key.txt that has your api key for accessing open-ai api's

### Packages:

*   `llamaindex` (version 0.5.1)
*   `pdfplumber`
*   `docx2txt`
*   `openai`
*   `llama-index-readers-file`
*   `sentence_transformers`
*   `ipython`

## Conclusion:

Upon comparison of the generated responses with the manual checking, the response is almost appropriate for the properly given query. Always response depends on the quality of query input that is fed to the system. Much more LLM integration with the quality input/query can make the system robust and close to the human thinking.

