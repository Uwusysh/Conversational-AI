## 📢 Conversational AI (Text, Voice, and RAG)

An intelligent, multi-input chatbot that supports both **text** and **voice** inputs, powered by **Groq's LLM**, **LangChain Retrieval-Augmented Generation (RAG)**, and **Gradio UI**. It also supports **vector-based document retrieval** from uploaded `.txt` files using **HuggingFace Embeddings**.

---

### 🚀 Features
- 🗣️ Speech-to-Text using `speech_recognition`
- 📄 File-based document retrieval with LangChain
- 🤖 RAG with Groq LLM (`llama3-8b-8192`)
- 🎯 Accurate and context-aware responses
- 🖼️ Clean Gradio UI (local only, no public sharing)

---

### 📦 Requirements

Make sure you have Python 3.8 or later.

Install the dependencies:
```bash
pip install -r requirements.txt
```

#### `requirements.txt` (create this file if you want):
```txt
gradio
torch
transformers
pydub
SpeechRecognition
python-dotenv
langchain
langchain-community
langchain-groq
```

---

### 🛠️ Setup Instructions

1. **Clone this repo (or copy the files):**

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. **Create your `.env` file** in the root directory:

```bash
touch .env
```

Paste your **Groq API Key** in the `.env`:
```env
GROQ_API_KEY=your_groq_api_key_here
```

3. **Run the app:**
```bash
python your_script_name.py
```

The Gradio interface will open in your browser (local only).

---

### 📁 How It Works

#### 🔉 Voice Mode:
- Record your voice.
- Audio is converted to text.
- Query is sent to Groq LLM using LangChain with document retrieval.

#### 💬 Text Mode:
- Type your message directly.
- Upload `.txt` files for custom context.
- LLM will search through those files using vector search before answering.

---

### 🧠 Tech Stack

| Component | Library |
|----------|----------|
| LLM      | `langchain-groq` |
| UI       | `gradio` |
| Voice Recognition | `speech_recognition` |
| Embeddings | `HuggingFaceEmbeddings` |
| Text Splitting | `RecursiveCharacterTextSplitter` |
| Vectorstore | `langchain` with temporary file loading |
| Env Management | `python-dotenv` |

---

### ⚠️ Notes
- Only `.txt` files are supported for document uploads.
- Audio must be in a compatible format (WAV recommended).
- The app does **not** expose a public link (`share=True` is disabled for privacy).

---

### 🙌 Acknowledgements
- [LangChain](https://www.langchain.com/)
- [Groq](https://groq.com/)
- [Gradio](https://gradio.app/)
- [HuggingFace](https://huggingface.co/)

---
## 📸 Example Output

Here is an example of the output you can expect from the API:

![Output Example](updated_policy_chatbot.py)

---
