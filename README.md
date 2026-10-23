# Beekeeping RAG - Knowledge Assistant

A Retrieval-Augmented Generation (RAG) project that answers beekeeping-related questions using information retrieved from a collection of beekeeping PDF documents.

The project implements the same core RAG workflow in two ways: a manual implementation and a LangChain-based implementation. It uses semantic embeddings and FAISS for document retrieval, with Gemini generating answers from the retrieved context.

## Project Overview

The goal of this project is to explore how RAG can connect a language model with a specialized knowledge base and provide answers grounded in relevant document excerpts.

The system follows these main steps:

1. **Document Processing:** Extract text from beekeeping PDF documents and clean the extracted content.
2. **Chunking:** Split the text into smaller chunks suitable for retrieval.
3. **Embedding Generation:** Convert text chunks into vector representations using `all-MiniLM-L6-v2` from Sentence Transformers.
4. **Vector Indexing:** Store the embeddings in a FAISS index for similarity-based retrieval.
5. **Context Retrieval:** Retrieve the most relevant chunks for a user's question.
6. **Answer Generation:** Provide the retrieved context to Gemini to generate a response.
7. **Source Verification:** Identify whether the answer is supported by the available knowledge base or whether the information cannot be verified from the retrieved context.

## Technologies Used

- **Python** - Core implementation
- **Sentence Transformers** - Text embeddings using `all-MiniLM-L6-v2`
- **FAISS** - Vector indexing and similarity search
- **Gemini API** - Context-based answer generation
- **LangChain** - Alternative implementation using RAG framework abstractions
- **Jupyter Notebook** - Development and experimentation

## Repository Structure

```text
beekeeping-rag/
├── README.md
├── evaluation/
│   └── evaluation_answers.md
└── notebooks/
    ├── Beekeeping_Assistant_manual_RAG.ipynb
    └── Beekeeping_Assistan_langchain_RAG.ipynb
```

## Implementations

### 1. Manual RAG Pipeline

[`Beekeeping_Assistant_manual_RAG.ipynb`](notebooks/Beekeeping_Assistant_manual_RAG.ipynb)

Implements the RAG workflow by handling the main stages directly, including document processing, chunking, embedding generation, FAISS indexing, retrieval, and answer generation.

### 2. LangChain RAG Pipeline

[`Beekeeping_Assistan_langchain_RAG.ipynb`](notebooks/Beekeeping_Assistan_langchain_RAG.ipynb)

Implements the RAG workflow using LangChain components, providing an alternative approach to organizing the document retrieval and question-answering process.

The two implementations demonstrate different ways to build a RAG system around the same general workflow.

## Evaluation

The system is evaluated manually using three questions:

- **Varroa mite prevention:** Tests retrieval and answer generation for a question covered by the knowledge base.
- **Hive health maintenance:** Tests the system's ability to retrieve relevant beekeeping practices.
- **Unsupported question:** Tests whether the system recognizes when the retrieved context does not contain the information needed to answer a question.

For each question, the evaluation records representative retrieved excerpts, the generated answer, the source status, and brief comments on retrieval relevance, answer quality, and grounding.

The evaluation is qualitative and intended to demonstrate the system's behavior on a small set of examples. It is not a comprehensive benchmark.

Detailed results are available in [`evaluation/evaluation_answers.md`](evaluation/evaluation_answers.md).

## Limitations

- Answer quality depends on the relevance and coverage of the source documents and retrieved chunks.
- The language model may generate information that is not supported by the retrieved context.
- The evaluation uses only three questions and is based on manual inspection.