# RAG Implementations For Wikipedia Search Assistant

#### The goal of this repository is to implement Wikipedia Search Assistant, by using Retrieval-Augmented Generation (RAG) pipeline to answer user queries by combining document retrieval with LLM. Two notebooks have different approaches:

#### The first notebook: 
Wikipedia articles are retrieved using the **WikipediaLoader** and converted into documents, with **HuggingFace embeddings** generated using a local model. The embeddings and metadata are stored in a **Chroma vector store**, enabling fast similarity-based document retrieval. A retriever fetches the most relevant documents, which are passed to OpenAI’s **GPT-4** via LangChain’s RetrievalQA chain to generate detailed answers. User queries are processed in batches, with retry mechanisms to handle API rate limits and ensure efficient processing. The Wikipedia Search Assistant provides clear, context-aware answers with source citations for transparency.

#### The second notebook: 

Wikipedia articles are again retrieved using the **WikipediaLoader** and converted into documents, with **OpenAI embeddings** generated. The embeddings and metadata are stored in a **FAISS vector store**, enabling fast similarity-based document retrieval. A retriever fetches the most relevant documents, which are passed to OpenAI’s **GPT-4o-mini** via LangChain’s RetrievalQA chain to generate detailed answers. The Wikipedia Search Assistant provides once again clear, context-aware answers with source citations for transparency.

#### If you find this repository useful for you, drop it a &#11088; :)
