# Watsonx RAG Chatbot 📚🤖

A Retrieval-Augmented Generation (RAG) chatbot built with **IBM Watsonx LLM**, **LangChain**, and **Chroma**.  
The chatbot can answer user queries from multiple product manuals (PDFs), remembers previous questions with conversational memory, and provides citations (document + page number).  

---

## 🚀 Features
- Load and process multiple PDF product manuals
- Chunk text with metadata:
  - Document name
  - Page number
  - Section heading (if available)
- Store embeddings in **Chroma** vector database
- Retrieval-Augmented Generation pipeline
- Conversational memory (multi-turn Q&A)
- Source citation (document + page number)
- Summarization function for manuals
- Gradio interface for interaction

---

## 🛠️ Tech Stack
- [IBM Watsonx.ai](https://www.ibm.com/watsonx) – LLM & Embeddings
- [LangChain](https://www.langchain.com/) – Orchestration
- [ChromaDB](https://www.trychroma.com/) – Vector Store
- [Gradio](https://www.gradio.app/) – UI
- [PyPDFLoader](https://pypi.org/project/pypdf/) – PDF ingestion

---

## 📂 Project Structure
📦 watsonx-rag-chatbot
┣ 📜 chatbot_notebook.ipynb # Main Jupyter Notebook
┣ 📜 app.py # Optional Gradio app version
┣ 📜 requirements.txt # Dependencies
┣ 📜 README.md # Project documentation
┗ 📂 manuals/ # Product manuals (PDFs)

yaml
Copy code

---

## ⚡ Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/your-username/watsonx-rag-chatbot.git
cd watsonx-rag-chatbot
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Add credentials
Create a cred.py file with your Watsonx credentials:

```bash
credentials = {
    "url": "YOUR_WATSONX_URL",
    "apikey": "YOUR_API_KEY"
}
model_id = "ibm/granite-13b-chat-v2"
credential_params = {
    "project_id": "YOUR_PROJECT_ID",
    "url": "YOUR_WATSONX_URL",
    "api_key": "YOUR_API_KEY",
    "username": "YOUR_USERNAME"
}
```
4. Run the notebook
```bash
jupyter notebook chatbot_notebook.ipynb
```
🎯 Example Interactions
Q: What is the warranty period of this product?
A: The warranty period is 1 year (document: manual1.pdf, page: 12).

Q: Does it cover labor?
A: Yes, the warranty covers both parts and labor (document: manual1.pdf, page: 13).

📌 Future Improvements
Add metadata-based filtering (restrict by manual or section)

Extend summarization for multi-document comparisons

Deploy on Hugging Face Spaces or IBM Cloud

📄 License
This project is licensed under the MIT License.
