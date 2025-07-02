# Text-Summarizer
This project is an advanced text processing app using Gradio and Hugging Face Transformers. It summarizes text, extracts keywords, answers questions, and provides metrics. It accepts text input from a textbox, file upload, or URL, and allows users to select models and customize summarization options.

# Deployment

## 🔗 Project Links

- 👉 [Click here to access the deployed application on Hugging Face Spaces](https://huggingface.co/spaces/somya-27-04-03/Text-Summarizer-Project)

- 👉 [Click here to view the full code on Google Colab](https://colab.research.google.com/drive/1spdf4YuYqWIuOyNE-cgz4OodrLF9lO9C?usp=sharing)

👥 Credits
-------------
🎯 **Deployment**
By: Somya Ranjan Mahapatra

Email: srm270405@gmail.com


💻 **Code & Design**
By: Debadatta Rout

Email: routdebadatta22@gmail.com


------

# My Text Summarizer screen (As i have designed it)

![image](https://github.com/user-attachments/assets/282414ab-2f91-455c-a247-36e48a2400c8)

![image](https://github.com/user-attachments/assets/856ff83a-3dc7-4590-bbc6-f580c2c4116b)

![image](https://github.com/user-attachments/assets/b97845ff-ac72-484f-a249-e63771d3c992)

![image](https://github.com/user-attachments/assets/77677f2b-dbe5-4ca8-87e6-975fa25ef3c5)

![image](https://github.com/user-attachments/assets/031c7b5c-8aad-4c3c-b1d3-6d03451b3519)

-----------------------------


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

![Image](https://github.com/user-attachments/assets/65628ee6-1651-469f-9911-e40e7f73cb4d)


This is a powerful and interactive **NLP-based web application** that performs **text summarization, keyword extraction, and question answering** using advanced deep learning models from Hugging Face Transformers.

Built with **Gradio**, this application provides a user-friendly interface to input raw text, upload documents, or extract content from a URL — and then processes the data to give you concise summaries, relevant keywords, and accurate answers to user queries.


---

## 🛠️ Features

- 📥 **Multi-modal Input Support**
  - Enter text manually in a textbox
  - Upload `.txt` or `.pdf` files
  - Provide a URL for automatic text scraping

- 🧾 **Text Summarization**
  - Supports **Abstractive** and **Extractive** summarization
  - User-defined summary length and format (paragraph/bullet points)
  - Choose summarization models dynamically

- 🧠 **Question Answering**
  - Ask any number of questions based on the input text
  - Supports follow-up questions using chat history
  - Displays model confidence scores

- 🔑 **Keyword Extraction**
  - Automatically extracts top-ranked keywords using **RAKE-NLTK**

- 📊 **Output Metrics**
  - Input word count
  - Summary word count
  - Compression rate
  - Readability score (Flesch Reading Ease)

- 💾 **Downloadable Outputs**
  - Download summary and Q&A session as `.txt` files

- 🧼 **Clear All**: Reset the entire interface with one click

---

## 🧠 NLP Concepts & Technologies Used

### 🔍 **Summarization Types**
- **Abstractive Summarization**: Generates new sentences that capture the meaning of the input text using a Transformer model.
- **Extractive Summarization**: Selects and ranks the most relevant sentences from the original text (uses NLTK sentence tokenization).

### 🤖 **Keyword Extraction**
- Uses **RAKE (Rapid Automatic Keyword Extraction)** via `rake-nltk` to extract the most relevant keyword phrases from the text.

### ❓ **Question Answering**
- Extractive QA: Locates the exact answer span from the input context.
- Conversation support: Maintains history for follow-up questions.

### 📐 **Readability & Metrics**
- Calculates:
  - Word counts (input vs summary)
  - Compression Rate: `% reduction from input to summary`
  - Readability Score: Flesch Reading Ease using `textstat`

---

## 🧰 Models Used

### 📝 **Summarization Models**
| Model Name | Description |
|------------|-------------|
| `facebook/bart-large-cnn` | A powerful abstractive summarization model fine-tuned on CNN/DailyMail |
| `t5-base` | A text-to-text transformer that performs multiple NLP tasks including summarization |

### ❓ **Question Answering Models**
| Model Name | Description |
|------------|-------------|
| `distilbert-base-uncased-distilled-squad` | Lightweight and fast QA model fine-tuned on SQuAD |
| `bert-base-cased-finetuned-squad` | Standard BERT model fine-tuned on SQuAD for QA tasks |

---




