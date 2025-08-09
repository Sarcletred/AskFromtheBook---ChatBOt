# AskFromtheBook---ChatBOt
An AI-powered chatbot that can answer any question from any book you upload.
This project is an interactive question-answering system that allows users to ask questions about the content of a PDF document. The system retrieves relevant information from the document using semantic search (FAISS) and generates answers using Groq’s Llama 3 language model via LangChain.
________________________________________
Features:
•	Load and process any PDF document.
•	Split text into manageable chunks for efficient search.
•	Generate text embeddings using Hugging Face sentence-transformers.
•	Store embeddings in a FAISS vector database for fast retrieval.
•	Use Groq's Llama 3 model to answer questions based on document content.
•	Interactive chat interface to ask questions and get AI-generated answers.
________________________________________
Technology Stack:
•	LangChain
•	Groq LLM (langchain-groq)
•	FAISS
•	Hugging Face Sentence-Transformers
•	PyPDF
•	Google Colab
________________________________________
How to Use:
1.	Open the Google Colab Notebook:
o	Use the provided link or upload the notebook to Google Colab.
2.	Install Required Libraries:
!pip install -q langchain groq faiss-cpu sentence-transformers pypdf
3.	Set Groq API Key:
from getpass import getpass
import os
os.environ["GROQ_API_KEY"] = getpass("Paste Groq API Key: ")
4.	Upload PDF Document:
from google.colab import files
uploaded = files.upload()
•	Select the PDF file you wish to use.
5.	Run the System:
o	The system will load the PDF, split the text, create embeddings, store them in FAISS, and set up the Groq language model.
o	Start the interactive Q&A session.
6.	Ask Questions:
o	Type any question related to the document's content.
Example:
Question: Who is Harry Potter's best friend?
Answer: Harry Potter's best friends are Ron Weasley and Hermione Granger.
________________________________________
Important Notes:
•	The PDF file is uploaded temporarily in Colab's environment and needs to be uploaded again each time the notebook is run.
•	The Groq API key must also be provided in each new session.
•	The system is designed for demonstration and educational purposes.
________________________________________
Credits:
•	LangChain
•	Groq
•	FAISS
•	Hugging Face Sentence-Transformers
•	PyPDF
________________________________________
Conclusion:
This project demonstrates how to build a powerful document-based question-answering system using semantic search and large language models. It provides an efficient way to retrieve information from documents and generate context-aware answers, making it suitable for applications like knowledge bots, document assistant
