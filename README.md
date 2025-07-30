# Conversational RAG with PDF Uploads and Chat History

This project implements a conversational Retrieval Augmented Generation (RAG) system using Streamlit, allowing users to upload PDF documents and engage in a chat with the content of those documents. The system maintains chat history for a more natural conversational flow.

## Features

*   **PDF Upload**: Easily upload one or multiple PDF files.
*   **Conversational AI**: Chat with the content extracted from the uploaded PDFs.
*   **Chat History**: The system remembers previous turns in the conversation, allowing for context-aware follow-up questions.
*   **Groq Integration**: Utilizes Groq for fast and efficient language model inference.
*   **HuggingFace Embeddings**: Uses `all-MiniLM-L6-v2` for generating document embeddings.
*   **Streamlit UI**: Provides an intuitive web interface for interaction.

## Setup and Installation

Follow these steps to set up and run the project locally:

### Prerequisites

*   Python 3.8+
*   `pip` (Python package installer)

### 1. Clone the Repository

```bash
git clone https://github.com/vishal_patel/RAG-Q-A-Conversation.git
cd RAG-Q-A-Conversation
```

### 2. Create a Virtual Environment (Recommended)

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

Create a `.env` file in the root directory of the project and add your Groq API key:

```
GROQ_API_KEY="your_groq_api_key_here"
HF_TOKEN="your_huggingface_token_here" # Optional, but good practice for HuggingFaceEmbeddings
```

Replace `"your_groq_api_key_here"` with your actual Groq API key. You can obtain one from the [Groq website](https://groq.com/).
The `HF_TOKEN` is optional for `HuggingFaceEmbeddings` but can be useful for rate limits or private models.

## Usage

To run the Streamlit application, execute the following command in your terminal:

```bash
streamlit run app.py
```

This will open the application in your web browser (usually at `http://localhost:8501`).

### How to Use:

1.  **Enter your Groq API Key**: Input your Groq API key into the provided text field.
2.  **Upload PDF Files**: Use the "Choose A PDF file" button to upload one or more PDF documents.
3.  **Enter Session ID**: (Optional) Provide a session ID to manage different chat histories. By default, it uses "default_session".
4.  **Ask Questions**: Once the PDFs are processed, type your questions into the "Your question:" input field and press Enter. The assistant will respond based on the content of the uploaded PDFs and the ongoing chat history.


