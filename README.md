# AI-Chatbot-Development-with-LLM
This is a RAG—based AI Chatbot focused on the diagnostic of Childhood Obesity. We developed it using Llama-2, FAISS Database and Fasttesxt Model


<img width="708" height="510" alt="image" src="https://github.com/user-attachments/assets/3eb57152-272d-4034-ac42-5ed561bea818" />

### LLaMA-2

LLaMA 2 is a series of pre-trained and fine-tuned large language models (LLMs) with parameter sizes ranging from 7 billion to 70 billion. Meta's fine-tuned LLMs, called **LLaMA 2-Chat**, are optimized for dialogue scenarios. LLaMA 2 models outperform most open-source conversational models on a variety of benchmarks and, according to human evaluations of usefulness and safety, may serve as suitable alternatives to closed-source models.

### FAISS Database

FAISS is an open-source vector database developed by Facebook (now Meta). It is designed as an efficient similarity search and clustering engine for dense vectors. The core of FAISS is written in C++ and relies on BLAS libraries. FAISS supports both CPU and GPU.  

The most important functionality of FAISS is **similar vector search**, where similarity between vectors can be measured using methods such as:

- L2 (Euclidean) distance  
- Inner product  

Storing vectors in FAISS involves adding them to its index structures. Most indices require training, which captures the distribution characteristics of the vectors.

### FastText Model

**FastText** is a lightweight and fast text processing and classification tool open-sourced by Facebook AI Research (FAIR) in 2016. It integrates some of the most successful ideas in natural language processing and machine learning, such as:

- Using bag-of-words and n-gram models to represent text  
- Sharing information across classes through hidden representations
<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/44336a2f-a4b5-412e-bc0d-d0892987ce7f" />
