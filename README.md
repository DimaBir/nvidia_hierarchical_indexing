# Hierarchical Indexing for Document Retrieval

This repository implements a hierarchical indexing system for document retrieval, leveraging OpenAI's GPT models and FAISS for vector storage. The application is containerized using Docker, with a Streamlit interface for querying documents.

## Introduction

This project showcases how hierarchical indexing can retrieve information quickly and accurately from large documents. Specifically, we use the entire `"Introduction to Algorithms, Third Edition" by Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest, and Clifford Stein.` book as our dataset. The book contains more than 1000+ pages. The hierarchical indexing method allows us to identify relevant sections through high-level summaries and then drill down into detailed chunks, ensuring that retrieval is fast and contextually relevant.

## Example Flow
<img src="Hierarchical_Retrieval_Schema.png" alt="Hierarchical Retrieval" width="50%">

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Git](https://git-scm.com/)

## Getting Started

1. Clone the repository to your local machine:

```bash
git clone https://github.com/DimaBir/hierarchical_indexing.git
cd hierarchical_indexing
```

2. Set up environment variables by creating a `.env` file in the *root* directory of the project and adding your environment variables:
```bash
OPENAI_API_KEY=your_openai_api_key_here
```

3. Build the Docker image using Docker Compose:
```bash
docker-compose build
```

4. Run the application:
```bash
docker-compose up
```

## Running the Application Without Docker
If you prefer to run the application without using Docker, follow these steps:  
1. If you prefer to run the application without using Docker, follow these steps:
```bash
git pull 
```
2. Navigate to the Project Directory
```bash
cd hierarchical_indexing
```
3. Set Up and Activate a Virtual Environment (optional but recommended):
4. Install the Required Dependencies:
```bash
pip install -r requirements.txt
```
5. Run the Streamlit Application:
```bash
streamlit run app.py
```
