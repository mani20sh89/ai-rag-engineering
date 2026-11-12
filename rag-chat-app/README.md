# InsureLLM – AI-Powered Knowledge Assistant

An interactive AI-powered knowledge assistant designed to answer questions about InsureLLM using Retrieval-Augmented Generation (RAG).

The application combines a conversational interface with context retrieval, allowing users to ask questions and receive answers supported by relevant information from the underlying knowledge base.

## Overview

InsureLLM Expert Assistant provides a chat-based interface for interacting with company knowledge.

Built with Gradio, the application displays two components side by side:

- **Conversation:** An interactive chatbot for submitting questions and viewing AI-generated responses.
- **Retrieved Context:** Displays the document passages used to generate the response, including their source information.

The application delegates question answering and document retrieval to a separate RAG implementation.

## Features

- Interactive conversational interface
- Retrieval-Augmented Generation (RAG) integration
- Context-aware question answering
- Retrieved document context displayed alongside responses
- Source information for retrieved documents
- Conversation history support
- Clean, responsive Gradio interface
- Copy support for chatbot messages

## Architecture

The application follows a retrieval-based question-answering workflow:

1. User submits a question through the Gradio interface.
2. The application passes the question and conversation history to the RAG implementation.
3. Relevant document context is retrieved.
4. The language model generates an answer using the retrieved context.
5. The response and supporting context are displayed in the interface.

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| User Interface | Gradio |
| RAG Integration | Custom LangChain implementation |
| Configuration | python-dotenv |
| Knowledge Retrieval | Vector database-backed retrieval |
| Language Model | Configured in the RAG implementation |

## Project Structure

```text
InsureLLM/
│
├── app.py
│
├── implementation/
│   └── answer.py
│
├── vector_db/
│
├── .env
├── requirements.txt
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd InsureLLM
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate the environment:

**macOS / Linux**
```bash
source .venv/bin/activate
```

**Windows**
```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root and add the credentials required by your RAG implementation.

Do not commit API keys or other secrets to version control.

### 5. Run the application

```bash
python app.py
```

The Gradio application launches locally and opens in your browser.

## Application Interface

The interface is organized into two panels:

**Conversation Panel**
- Submit questions about InsureLLM.
- View responses in a conversational format.
- Maintain conversation history.

**Retrieved Context Panel**
- Inspect relevant retrieved passages.
- View the source associated with each document.
- Understand the information used to generate responses.

## Engineering Concepts

This project explores practical implementation of:

- Retrieval-Augmented Generation (RAG)
- Context-aware LLM applications
- Conversational AI interfaces
- Document retrieval and source attribution
- Separation of application UI and RAG logic
- Environment-based configuration

## Purpose

This project demonstrates the integration of a retrieval-based AI question-answering system with an interactive conversational interface.

It forms part of a broader exploration of AI Engineering, focusing on building practical applications using LLMs, retrieval pipelines, and modern Python frameworks.
