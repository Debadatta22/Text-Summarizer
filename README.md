# Text-Summarizer
This project is an advanced text processing app using Gradio and Hugging Face Transformers. It summarizes text, extracts keywords, answers questions, and provides metrics. It accepts text input from a textbox, file upload, or URL, and allows users to select models and customize summarization options.
------
# Project Description
This project is an advanced text processing application built using Gradio and various natural language processing libraries such as Hugging Face Transformers, RAKE-NLTK, NLTK, and TextStat. It provides a user-friendly web interface to perform the following tasks:

**Text Input:** Users can input text by pasting it directly into a textbox, uploading a .txt or .pdf file, or providing a URL for web scraping.

**Text Summarization:** The application supports both Abstractive (using models like BART Large CNN or T5 Base) and Extractive summarization. Users can control the length of the summary and choose between paragraph or bullet point format.

**Keyword Extraction:** Key phrases are extracted from the input text using RAKE-NLTK.

**Question Answering:** Users can ask questions based on the provided text using models like DistilBERT SQuAD or BERT Base Cased SQuAD. The application supports follow-up questions and provides confidence scores for the answers.

**Output Metrics:** Various metrics are calculated and displayed, including input word count, summary word count, compression rate, and readability score (Flesch Reading Ease).

**Model Selection:** Users can select their preferred models for summarization and question answering from available options.

The application is designed to be interactive and provides clear instructions on how to use its features.

-------


# Section 1: Environment Setup and Installation
This part of your project ensures that all necessary Python libraries and tools are installed for the text summarization app to run smoothly. 

Here's a detailed breakdown of what's happening:

**Installed Libraries**

**Gradio**
For creating an interactive web-based UI.

**Transformers**
From Hugging Face — used for advanced NLP models like BART, T5, DistilBERT, etc.

**RAKE-NLTK**
RAKE (Rapid Automatic Keyword Extraction) + NLTK for extracting key phrases.

**TextStat**
Computes readability scores like Flesch Reading Ease.

**pypdf / pdfplumber**
For parsing and extracting text from .pdf files.

**BeautifulSoup4 + Requests**
To scrape and extract content from URLs (web pages).

**newspaper3k**
(Optional add-on) for smarter article extraction.

**python-docx**
For .docx file support (if needed in future).

**langdetect**
For detecting the language of the input (could be helpful in a multilingual setup).

**torch + accelerate**
Backend support for running transformer models efficiently.

**google-auth, oauthlib, httplib2**
Authentication tools, potentially useful if you plan to use Google APIs later.

**Requirements File** (requirements.txt)

**NLTK Downloads**

ensuring that all required NLTK resources are downloaded:

**punkt** – Tokenizer for breaking text into sentences/words.

**stopwords** – List of common stopwords used in keyword extraction and filtering.

**punkt_tab** – Possibly needed for tokenization metadata.

Also handled SSL-related download issues using Python’s ssl module — good practice for cross-platform compatibility.

Successfully built a feature-rich, production-level text summarization and question answering app with a modular, scalable architecture.

------------

# Section 2: Full Application Code

📥 **Input Handling:** .txt, .pdf, URLs, or direct text input.

🧠 **Model Handling:** Dynamic, cacheable loading of summarization and QA models.

📝 **Summarization:** Abstractive (with model) and Extractive (with NLTK).

🔑 **Keyword Extraction:** RAKE-based, with NLTK support.

❓ **Q&A:** DistilBERT / BERT extractive QA with confidence and follow-up support.

📊 **Metrics:** Word counts, compression rate, Flesch readability score.

💾 **File downloads:** For summary and QA.

🧼 **UI:** Interactive Gradio interface with radio buttons, sliders, and chatbot.

🔄 Clear functionality to reset all fields.

----------------

# Flowchart Idea: "Text Processing App - Workflow

It can be divide it into 3 main stages:

1. Input Handling
2.  Preprocessing & Analysis & Core NLP Tasks
3.  Output & Interaction
