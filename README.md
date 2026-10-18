PDF Question-Answering System (RAG-Based)

A Retrieval-Augmented Generation (RAG) application that allows users to upload PDF documents and ask context-based questions about their contents.

Built using Python, Streamlit, LangChain, Ollama, and ChromaDB, the application extracts text from PDFs, retrieves relevant information, and generates answers using a locally running Large Language Model (LLM).

✨ Key Features

* 📂 PDF Upload: Upload PDF documents through an interactive web interface.
* 📝 Text Extraction: Extract text from uploaded PDF files.
* ✂️ Text Chunking: Divide extracted text into smaller, manageable chunks for efficient retrieval.
* 🔎 Semantic Search: Retrieve relevant document sections using vector embeddings and similarity search.
* 🧠 LLM-Powered Answers: Generate context-aware responses using the Llama 3.1 language model.
* 💬 Question Answering: Ask questions about the uploaded document and receive answers based on its content.
* 🖥️ Interactive Interface: Use the application through a Streamlit web interface.
* 🔒 Local Processing: Run the language model and embedding model locally through Ollama.
* 🗑️ Temporary File Handling: Process uploaded PDFs using temporary files.

🛠️ Technologies Used

Technology	Purpose
Python	Core application logic
Streamlit	Interactive web interface
LangChain	RAG pipeline and document processing
Ollama	Run language models locally
Llama 3.1	Generate answers to user questions
Nomic Embed Text	Convert text into vector embeddings
ChromaDB	Store embeddings and retrieve relevant document chunks
PyPDF	Extract text from PDF documents

⚙️ How It Works

The application follows a Retrieval-Augmented Generation (RAG) workflow.

1. PDF Upload: The user uploads a PDF document.
2. Text Extraction: PyPDFLoader extracts text from the document.
3. Text Chunking: RecursiveCharacterTextSplitter divides the extracted text into smaller chunks.
4. Embedding Generation: The embedding model converts the chunks into numerical vector representations.
5. Vector Storage: Chroma stores the document embeddings for similarity-based retrieval.
6. Question Processing: The user enters a question related to the uploaded document.
7. Context Retrieval: The system retrieves relevant document chunks using similarity search.
8. Answer Generation: Llama 3.1 uses the retrieved context and the user’s question to generate a response.
9. Answer Display: The response is displayed in the Streamlit interface.

🏗️ Project Architecture

User Uploads PDF
       |
       v
PDF Text Extraction
       |
       v
Text Chunking
       |
       v
Embedding Generation
       |
       v
Chroma Vector Store
       |
       v
User Question
       |
       v
Similarity Search
       |
       v
Relevant Context + Question
       |
       v
Llama 3.1 via Ollama
       |
       v
Context-Based Answer
       |
       v
Streamlit Interface

📁 Project Structure

PDF-QA-RAG-System/
│
├── app.py
├── requirements.txt
├── README.md
└── LICENSE

* app.py — Contains the application logic, PDF processing, text chunking, vector storage, retrieval, and answer generation.
* requirements.txt — Lists the Python dependencies required by the application.
* README.md — Provides project documentation and setup instructions.

📋 Prerequisites

Before running the application, ensure that you have:

* Python installed on your system.
* Ollama installed and running locally.
* The required Ollama models downloaded.
* The Python packages listed in requirements.txt.

Required Ollama Models

The application uses the following models:

* llama3.1 — For generating answers.
* nomic-embed-text — For generating text embeddings.

Download the models using:

ollama pull llama3.1
ollama pull nomic-embed-text

Ollama can be installed from the official Ollama website.

🚀 Installation and Setup

1. Open the Project Folder

Open the project folder in VS Code and launch its integrated terminal.

2. Create a Virtual Environment

python -m venv venv

3. Activate the Virtual Environment

For Windows:

venv\Scripts\activate

4. Install Dependencies

pip install -r requirements.txt

5. Install Ollama Models

Ensure Ollama is installed and running, then execute:

ollama pull llama3.1
ollama pull nomic-embed-text

6. Run the Application

streamlit run app.py

7. Open the Application

Streamlit will provide a local URL, usually:

http://localhost:8501

Open the URL in your browser to access the application.

💡 How to Use

1. Start the application using streamlit run app.py.
2. Open the Streamlit URL in your browser.
3. Upload a PDF document using the file uploader.
4. Enter a question related to the document.
5. Allow the application to process the PDF and retrieve relevant information.
6. View the generated answer in the interface.
7. Ask questions about different sections of the uploaded document.

Example question:

What is the main conclusion of this research paper?

Other possible questions include:

* What are the main objectives of this document?
* Summarize the key findings.
* What methodology was used?
* What conclusions does the document present?

The quality of the answers depends on the PDF’s extracted text, the retrieved context, and the language model’s response.

📚 Applications

This type of document question-answering system can be useful for:

* Research papers and academic literature.
* Technical reports and project documentation.
* Study notes and educational materials.
* Manuals and reference documents.
* Reports containing information that users need to retrieve quickly.

🔧 Future Improvements

Potential enhancements include:

* Support for uploading multiple PDF documents.
* Displaying source pages or document excerpts alongside answers.
* Adding conversation history for follow-up questions.
* Improving error handling for scanned PDFs and empty documents.
* Adding document previews and a more informative user interface.
* Evaluating retrieval quality and answer accuracy on a test set.
* Deploying the application to a suitable hosting platform.

🙌 Acknowledgements

This project uses the following open-source technologies:

* Streamlit — Web application interface.
* LangChain — Document processing and RAG components.
* Ollama — Local language model execution.
* ChromaDB — Vector storage and similarity search.
* Nomic Embed Text — Text embedding model.
* PyPDF — PDF text extraction.

⸻

