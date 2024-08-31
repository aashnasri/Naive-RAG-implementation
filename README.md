Simple RAG(Retrieval Augmented Generation) system

Overview

This code Implements a simple Retrieval-Augmented Generation (RAG) system for processing and querying text documents. The complete modules aim to get an understanding a naive implementation without using a vector db.

Components

Installing required libraries - The main libraries include components of building RAG, like text splitters, openai, runnables, transformers, prompt etc
Importing relevant libraries - The main libraries include components of building RAG, like text splitters, openai, runnables, transformers, prompt etc
Import tokens - Load the documents/files from the directory from which we want to retrieve the responses.
Chunker - Create chunks of the documents, every chunk will have a chunk ID stored in a document ID , we can define the chunk size
Embedding - Use openai model to create embeddings of the chunks created above
Similarity score - Retreiver class contains a cosine similarity function which will generate a similarity score between the document embeddings and the prompt. The top 3 embeddings which have a high similarity score will be retreiver by the retriever.
LLM - The openai gpt model will take the retriever output and the prompt as the user query and return the output response.
Benefits of the code

Simple implementation of text chunking and retrieval
Modularized structure
Scalable
Processing History, so that LLM can continue conversation
Further improvements

Implement advanced text splitters
Vector db approach for efficient storage of embedings
Auto processing of history
