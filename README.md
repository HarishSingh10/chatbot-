# 📚 Chat with PDF using LLaMA 2 + Groq + Streamlit

Interact with any PDF document using natural language! This app uses **LLaMA 2 via Groq**, **LangChain**, **FAISS**, and **Streamlit** to let you ask questions about your PDF — with optional **voice input** too! 🎤

---

## 🚀 Features

- 📄 Upload and read any PDF
- 🧠 Ask questions about the content
- 🔍 Uses semantic search with FAISS and HuggingFace embeddings
- 🤖 Powered by LLaMA 2 (via Groq API)
- 💬 Voice input support using SpeechRecognition
- 🔁 Remembers chat history during session

---

## 📦 Tech Stack

- [Streamlit](https://streamlit.io/)
- [LangChain](https://www.langchain.com/)
- [FAISS](https://github.com/facebookresearch/faiss)
- [Groq API](https://console.groq.com/)
- [LLaMA 2](https://ai.meta.com/llama/)
- [PyPDF2](https://pypi.org/project/PyPDF2/)
- [SpeechRecognition](https://pypi.org/project/SpeechRecognition/)

---

## 🖥️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/HarishSingh10/Chat-PDF.git
cd Chat-PDF
```

### 2. Create `.env` File

Create a `.env` file in the project root and add your Groq API key:

```env
LLAMA_API_KEY=your_groq_api_key_here
```

> 🔐 **Never share your API key publicly.**

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

If you get errors with `pyaudio`, you may need:

```bash
# Windows (using pre-built wheel)
pip install pipwin
pipwin install pyaudio

# Or macOS/Linux (with portaudio)
brew install portaudio  # or sudo apt install portaudio19-dev
pip install pyaudio
```

### 4. Run the App

```bash
streamlit run app.py
```

---

## 🗣️ Voice Input

Click on the **"🎤 Use Voice Input"** button to speak your question instead of typing.

> Make sure your microphone is enabled and permissions are granted in your browser.

---

## 🧠 How It Works

1. Upload a PDF → Text is extracted using **PyPDF2**
2. Text is split into chunks and embedded with **HuggingFace Embeddings**
3. Chunks are stored in a **FAISS** vector store
4. **LangChain**'s `ConversationalRetrievalChain` handles memory + LLM response
5. Queries are answered by **Groq LLaMA 2 (gemma2-9b-it)**

---

## 📁 Project Structure

```
📁 Chat-PDF/
│
├── app.py                  # Streamlit app script
├── .env                    # Your Groq API key (DO NOT COMMIT)
├── requirements.txt        # Dependencies
├── README.md               # You're reading it :)
└── ...
```

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🙋‍♂️ Author

Built with ❤️ by [Harish Singh](https://github.com/HarishSingh10)

---

## 🌟 Star this repo if you find it useful!
