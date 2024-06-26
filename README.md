# Chat with PDF using Streamlit and Google Gemini

Welcome to the Chat with PDF project! This application allows users to upload PDF documents and interact with them by asking natural language questions. The app uses several state-of-the-art tools and technologies to provide accurate and detailed responses.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Tools and Technologies](#tools-and-technologies)
- [How It Works](#how-it-works)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project leverages the power of machine learning and artificial intelligence to create an interactive PDF chatbot application. By combining several advanced libraries and frameworks, it enables users to upload PDF files, extract text, create embeddings, and interact with the content via a conversational interface.

## Features

- Upload multiple PDF files
- Extract text from PDFs
- Split text into manageable chunks
- Generate embeddings for text chunks
- Store and search embeddings using FAISS
- Interact with PDF content using a conversational AI model
- Receive detailed and context-aware answers to user questions

## Tools and Technologies

### Streamlit
A powerful open-source app framework for Machine Learning and Data Science projects. It provides an easy way to build and share web apps with just a few lines of code.

### PyPDF2
A Python library to read and extract text from PDF files.

### LangChain
A framework for developing applications powered by language models. This project uses:
- **RecursiveCharacterTextSplitter**: To break down the extracted PDF text into manageable chunks.
- **GoogleGenerativeAIEmbeddings**: For creating embeddings using Google’s generative AI model.
- **FAISS**: A library for efficient similarity search and clustering of dense vectors, used to store and search text embeddings.
- **ChatGoogleGenerativeAI**: A conversational AI model from Google’s Gemini suite for generating responses.

### Google Generative AI (Gemini)
Provides the language models and embedding capabilities necessary for understanding and generating human-like text.

### dotenv
To manage environment variables securely.

## How It Works

1. **Upload PDFs**: Users can upload multiple PDF files through the Streamlit interface.
2. **Extract Text**: The PyPDF2 library reads and extracts text from each uploaded PDF.
3. **Text Chunking**: The extracted text is split into chunks using LangChain’s RecursiveCharacterTextSplitter to ensure efficient processing and storage.
4. **Generate Embeddings**: Each text chunk is converted into embeddings using Google Generative AI’s embedding model.
5. **Vector Store**: These embeddings are stored in a FAISS index, enabling fast and efficient similarity searches.
6. **Conversational AI**: When a user asks a question, the application searches the FAISS index for relevant text chunks and uses Google’s conversational AI model to generate a detailed response.
7. **Interactive Q&A**: The user can interact with the PDF content through a conversational interface, asking questions and receiving detailed, context-aware answers.

## Setup and Installation

### Prerequisites

- Python 3.7+
- Streamlit
- PyPDF2
- LangChain
- Google Generative AI SDK
- FAISS
- dotenv

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/chat-with-pdf.git
cd chat-with-pdf
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate # On Windows use `venv\Scripts\activate`
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Set up your environment variables by creating a `.env` file in the root directory and adding your Google API key:

```
GOOGLE_API_KEY=your_google_api_key
```

## Usage

1. Run the Streamlit application:

```bash
streamlit run app.py
```

2. Open your browser and go to `http://localhost:8501`.

3. Use the sidebar to upload your PDF files and click on the "Submit & Process" button.

4. Ask questions in the main interface and get detailed answers from the uploaded PDFs.

## Future Enhancements

- Improve the model’s accuracy and response quality.
- Explore more advanced AI models and integrations.
- Make the application more robust and user-friendly.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.

