# AI-Chatbot-Development-with-LLM
This is a RAG—based AI Chatbot focused on the diagnostic of Childhood Obesity. We developed it using Llama-2, FAISS <br>
Database and FastText Model. The entire code can be found at **aidoctor(1).ipynb**, the detailed explaination of the code <br> 
can be found at **LLM_code_description.pdf**.


<img width="708" height="510" alt="image" src="https://github.com/user-attachments/assets/3eb57152-272d-4034-ac42-5ed561bea818" />

## Terminologies 

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

## Structure Introduction

The overall model framework can be divided into **four main modules**:

### 1. Input Dataset Construction
To provide professional and accurate responses specifically targeting childhood obesity, we build a **custom dataset**. Data is collected from reputable journals and authoritative websites. Using the **LangChain** framework, these PDF-formatted documents are processed and stored in a **FAISS database** for efficient similarity search.

### 2. Large Language Model Configuration and Download
We select an appropriate model configuration and download the required large language model from **Hugging Face**. In this project, we use **Llama**, which offers strong performance in AI conversational tasks and is particularly suited for medical consultation scenarios.

### 3. Text Classification Model Training
To enhance the relevance of responses, we train a **FastText** model on our custom dataset. This model filters out user queries unrelated to childhood obesity, improving response accuracy and overall user experience.

### 4. Model Fine-tuning
To further optimize the large language model for our target task, we perform **supervised fine-tuning** using over 3,000 highly relevant training examples. This fine-tuning adjusts model parameters to specialize in answering questions related to obesity.

---

### Workflow
1. **Query Classification**:  
   User queries are first passed through the text classification model.  
   - If the query is unrelated to childhood obesity, the chatbot outputs a predefined response.  
   - If the query is related, the system retrieves **highly relevant data** from the FAISS database using similarity search.

2. **Contextual Answer Generation**:  
   The retrieved data is then fed into the **large language model**, which summarizes and integrates the information to provide a **final professional answer** to the user.

<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/44336a2f-a4b5-412e-bc0d-d0892987ce7f" />


