# Fancy Mesop Chat

A modern, interactive chatbot application built using the **[Mesop](https://mesop-dev.github.io/mesop/)** framework and **Gemma 3 4B** model via **Ollama** for local inference. This application provides a sleek chat interface with advanced features like conversation history, message rating, and responsive design.

## 📸 Demo

![Fancy Mesop Chat Interface](https://github.com/user-attachments/assets/your-screenshot-url-here)

*The chat interface showing a conversation about AI history, with features like chat history sidebar, message rating buttons, and dark mode theme.*

---

## 🚀 Features

- 🤖 **AI-Powered Chat**: Integrates with Gemma 3 4B model via Ollama
- 💬 **Interactive UI**: Clean, modern chat interface with Material Design components
- 📱 **Responsive Design**: Mobile-friendly interface that adapts to different screen sizes
- 📋 **Chat History**: Save and manage multiple conversation sessions
- 👍 **Message Rating**: Rate bot responses with thumbs up/down
- 🔄 **Message Regeneration**: Regenerate bot responses if unsatisfied
- � **Theme Toggle**: Switch between light and dark modes
- ⌨️ **Keyboard Shortcuts**: Use Shift+Enter to send messages quickly
- � **Example Prompts**: Quick-start with predefined example queries
- 🔒 **Local-First**: All processing happens locally for privacy

---

## 📦 Tech Stack

- **Framework**: [Mesop](https://mesop-dev.github.io/mesop/) - Python-based UI framework
- **AI Integration**: [LangChain Ollama](https://python.langchain.com/docs/integrations/llms/ollama)
- **Model**: Gemma 3 4B (locally hosted via Ollama)
- **UI Components**: Material Design via Mesop
- **Language**: Python 3.10+

---

## 🧰 Requirements

- **Python**: 3.10 or higher
- **Ollama**: Installed and running locally
- **Gemma 3 4B Model**: Downloaded via Ollama

### Dependencies
- `mesop` - UI framework
- `langchain-ollama` - Ollama integration for LangChain

---

## ⚙️ Installation & Setup

### 1. Install Ollama
First, install Ollama on your system:
```bash
# On macOS
brew install ollama

# On Linux
curl -fsSL https://ollama.com/install.sh | sh

# On Windows
# Download from https://ollama.com/download
```

### 2. Download Gemma 3 4B Model
```bash
ollama pull gemma2:2b
# Note: The code uses "gemma3:4b" but you may need to adjust based on available models
# Check available models with: ollama list
```

### 3. Clone and Setup Project
```bash
# Clone the repository
git clone <your-repository-url>
cd Chat-Application

# Create virtual environment
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate

# Install Python dependencies
pip install mesop langchain-ollama
```

### 4. Run the Application
```bash
# Start Ollama service (if not already running)
ollama serve

# In another terminal, run the Mesop app
python main.py
```

The application will be available at `http://localhost:32123` (or the port shown in terminal).

---

## 🎯 Usage

### Basic Chat
1. Open the application in your browser
2. Type your message in the text area at the bottom
3. Press **Shift+Enter** or click the send button
4. Wait for the AI response

### Advanced Features
- **Rate Messages**: Use 👍/👎 buttons to rate bot responses
- **Regenerate**: Click the ↻ button to regenerate a response
- **New Chat**: Click the + button in the sidebar to start fresh
- **Chat History**: Access previous conversations from the sidebar
- **Theme Toggle**: Switch between light/dark mode using the theme button
- **Example Prompts**: Click on example queries to get started quickly

### Keyboard Shortcuts
- **Shift+Enter**: Send message
- **Focus**: Auto-focus on input after actions

---

## 🔧 Configuration

### Changing the AI Model
To use a different Ollama model, modify the model initialization in `main.py`:

```python
# Current configuration
model = OllamaLLM(model="gemma3:4b")

# Example alternatives
model = OllamaLLM(model="llama2")           # LLaMA 2
model = OllamaLLM(model="mistral")          # Mistral
model = OllamaLLM(model="codellama")        # Code Llama
```

### Customizing the UI
- **App Title**: Modify `_APP_TITLE` constant
- **Avatar**: Change `_BOT_AVATAR_LETTER` 
- **Examples**: Update `_EXAMPLE_USER_QUERIES` tuple
- **Styling**: Adjust Mesop styles throughout the code

---

## 📁 Project Structure

```
Chat-Application/
├── main.py              # Main application file
├── README.md           # This file
├── env/                # Virtual environment (created after setup)
└── __pycache__/        # Python cache files
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🔗 Useful Links

- [Mesop Documentation](https://mesop-dev.github.io/mesop/)
- [Ollama Documentation](https://ollama.com/)
- [LangChain Ollama Integration](https://python.langchain.com/docs/integrations/llms/ollama)
- [Gemma Model Information](https://ai.google.dev/gemma)

---

## ⚠️ Troubleshooting

### Common Issues

1. **Ollama not found**: Ensure Ollama is installed and in your PATH
2. **Model not available**: Check available models with `ollama list`
3. **Port conflicts**: Mesop may use different ports; check terminal output
4. **Slow responses**: Ensure sufficient RAM for the model (4GB+ recommended for Gemma 3 4B)
