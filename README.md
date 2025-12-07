# AI-Powered HR Policy Assistant
*A retrieval-augmented chatbot that turns static HR policies into conversational knowledge.*

---

## 📘 Overview

This project was developed as part of my **Applied Generative AI Specialization** coursework.  
The assignment required building a practical Retrieval-Augmented Generation (RAG) system using real documents—in this case, a company HR policy PDF.

The result is an **AI-powered HR Assistant** that answers employee questions by retrieving the most relevant sections of the policy and generating grounded, accurate responses. It demonstrates how generative AI can reduce operational load in HR teams by transforming static documents into interactive intelligence.

---

## ✨ Key Features

### 🔍 Document Ingestion & Parsing
- Loads an HR policy PDF using LangChain’s `PyPDFLoader`
- Splits the text into overlapping chunks for more accurate retrieval

### 🧠 Vector Embeddings & Storage
- Generates embeddings using the OpenAI Embeddings API
- Stores vectors in a **ChromaDB** database for efficient similarity search

### 🤖 RAG-Based Question Answering
- Retrieves the top policy chunks related to a user's question
- Passes retrieved context + question into an OpenAI ChatCompletion call
- Produces grounded, policy-aligned answers (minimizing hallucinations)

### 💬 Interactive UI
- A Gradio-powered interface lets users chat with the assistant
- Answers include the supporting text retrieved from the PDF

---

## 🛠️ Technologies Used

- **Python**
- **LangChain**
- **ChromaDB**
- **RAG**
- **OpenAI API** (chat completions + embeddings)
- **Gradio**
- **PyPDFLoader**
- **Google Colab**

---

## 📂 Project Structure
├── AI_Powered_HR_Assistant.ipynb # Full end-to-end notebook  
├── data/  
│   └── HR_Policy.pdf # Example policy document  
├── README.md # Project documentation  


---

## 🚀 How It Works

1. **Upload the HR policy PDF**  
   LangChain loads and parses the document.

2. **Chunk the document**  
   Text is split into overlapping segments preserving context.

3. **Generate embeddings**  
   Each chunk is converted into a vector using the OpenAI embeddings model.

4. **Store embeddings in ChromaDB**  
   Enables fast similarity search for relevant policy text.

5. **Ask questions in Gradio**  
   - Retrieves the top-k most relevant chunks  
   - Sends user question + retrieved context to the LLM  
   - Returns an accurate, grounded answer  

---

## 📌 Example Questions You Can Ask

- “What is the parental leave policy?”
- “How many vacation days do employees receive?”
- “What is the disciplinary process?”
- “Does the company allow flexible working arrangements?”

Each response is supported by retrieved policy text.

---

## 🎯 Why This Project Matters

Although this originated as a class assignment, the architecture reflects real enterprise AI patterns:

- Organizations store critical knowledge in PDFs or SharePoint folders.
- Employees spend time searching (or guessing) instead of accessing accurate information.
- Even a lightweight RAG workflow can improve accuracy, consistency, and response time.

This project shows how **AI can augment—not replace—human intelligence** in HR and compliance workflows.

---

## 🔧 Setup & Running Instructions

### 1. Install dependencies
```bash
pip install langchain openai chromadb gradio pypdf

```
### 2. Add your OpenAI API key
```python
os.environ["OPENAI_API_KEY"] = "your_key_here"
```
### 3. Run the notebook

Open and execute each cell in:
**AI_Powered_HR_Assistant.ipynb**

### 4. Launch the Gradio app

```python
gradio_interface.launch()
```

---

## 📝 Attribution

This project was developed as part of the **Applied Generative AI Specialization**, Purdue University.
All implementation, experimentation, and documentation reflect my original work based on course-provided requirements.

---

## 📫 Contact

For more projects, frameworks, and hands-on experiments in applied AI, visit **AI with Aimee** https://ai-with-aimee.lovable.app/.

---
