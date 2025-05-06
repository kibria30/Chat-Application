# Chat Application

A chatbot application built using the open-source **[mesop](https://mesop-dev.github.io/mesop/)** framework and **open-source large language models (LLMs)** such as **Gemma**, **LLaMA**, and **Qwen**, integrated via **Ollama** for local inference and flexible deployment.

---

## 🚀 Features

- 🤖 AI-powered conversational chatbot
- 🧠 Plug-and-play with open-source LLMs via Ollama
- 🛠 Built with [mesop](https://mesop-dev.github.io/mesop/), a lightweight Python framework for UI apps
- 🌐 Local-first and privacy-friendly
- 🔁 Easily switch between supported LLMs like Gemma, LLaMA, and Qwen

---

## 📦 Tech Stack

- **Backend & UI**: Python + [mesop](https://mesop-dev.github.io/mesop/)
- **Model Runtime**: [Ollama](https://ollama.com/)
- **LLMs**: Gemma, LLaMA, Qwen (run locally via Ollama)

---

## 🧰 Requirements

- Python 3.9+
- [Ollama](https://ollama.com/) installed and running
- mesop

---

## ⚙️ Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/chat-application.git
cd chat-application

# Set up virtual environment
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate

# Install dependencies
pip install mesop
