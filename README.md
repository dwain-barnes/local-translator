# Local Translator

![Local Translator](https://img.shields.io/badge/AI-Translation-blue)
![Ollama](https://img.shields.io/badge/Ollama-Powered-green)
![Languages](https://img.shields.io/badge/Languages-55-orange)

A private, local AI-powered translation application that runs entirely on your computer. Translate text, documents, and images across 55 languages without sending any data to external servers.

## ✨ Features

- 🔒 **100% Private & Local** - All translations happen on your computer, no data sent to external servers
- 🌍 **55 Languages** - Support for major world languages including English, Welsh, Spanish, French, German, Chinese, Japanese, Arabic, and more
- 📄 **Multiple File Formats**
  - Text files (.txt)
  - PDF documents (.pdf)
  - Word documents (.docx)
  - Images (.png, .jpg, .jpeg, .gif, .webp) - Extract and translate text from images
- 🎯 **Easy to Use** - Simple drag-and-drop interface
- ⚡ **Fast** - Powered by local AI models (no internet required after setup)
- 🎨 **Clean UI** - Google-inspired design with dark/light mode support

## 🚀 Quick Start

### Prerequisites

1. **Install Ollama** - [Download from ollama.com](https://ollama.com)
2. **Download translateGemma Model**
   ```bash
   ollama pull translategemma:27b
   ```
   Or use smaller models:
   - `ollama pull translategemma` (4B - 3.3GB)
   - `ollama pull translategemma:12b` (8.1GB)

### Usage

1. **Download** the `local-translator.html` file
2. **Open** it in your web browser (Chrome, Firefox, Edge, etc.)
3. **Upload** a file or type text directly
4. **Select** source and target languages
5. **Click** "Translate"

That's it! No installation, no setup, just open and use.

## 📋 Supported Languages

English, Afrikaans, Arabic, Bulgarian, Bengali, Catalan, Czech, Welsh, Danish, German, Greek, Spanish, Estonian, Persian, Finnish, French, Irish, Scottish Gaelic, Galician, Gujarati, Hebrew, Hindi, Croatian, Hungarian, Indonesian, Italian, Japanese, Kannada, Korean, Lithuanian, Latvian, Macedonian, Malayalam, Marathi, Malay, Maltese, Dutch, Norwegian, Polish, Portuguese, Romanian, Russian, Slovak, Slovenian, Albanian, Serbian, Swedish, Swahili, Tamil, Telugu, Thai, Turkish, Ukrainian, Urdu, Vietnamese, Chinese (Simplified), Chinese (Traditional)

## 🖼️ Screenshots

### Main Interface
Clean, intuitive interface with drag-and-drop file support

### Translation in Action
Real-time translation with support for multiple file formats

### Settings
Choose between different model sizes based on your needs

## 💡 How It Works

1. **Local AI Processing** - Uses Google's translateGemma model via Ollama
2. **No Internet Required** - After downloading the model, everything runs offline
3. **Privacy First** - Your documents and text never leave your computer
4. **Smart Extraction** - Automatically extracts text from PDFs, Word docs, and images

## 🛠️ Technical Details

### Architecture
- **Frontend**: Single HTML file with vanilla JavaScript
- **AI Engine**: Ollama (local LLM runtime)
- **Model**: Google's translateGemma (4B/12B/27B variants)
- **APIs Used**: Ollama REST API

### File Processing
- **PDF**: pdf.js for text extraction
- **Word**: mammoth.js for .docx parsing
- **Images**: Base64 encoding with vision-enabled translation

### Model Options
| Model | Size | RAM Required | Speed | Quality |
|-------|------|--------------|-------|---------|
| translategemma | 3.3GB | 8GB | Fast | Good |
| translategemma:12b | 8.1GB | 16GB | Medium | Better |
| translategemma:27b | 17GB | 32GB | Slower | Best |

## 🔧 Configuration

The application auto-detects Ollama running on `http://localhost:11434`. If you're running Ollama on a different port or host, you can change it in the Settings section.

## 🎯 Use Cases

- **Document Translation** - Translate research papers, reports, and documents
- **Learning Languages** - Practice translations and compare results
- **Privacy-Sensitive Content** - Translate confidential documents without cloud services
- **Offline Translation** - Work without internet connectivity
- **Batch Processing** - Translate multiple files quickly
- **Image Text Translation** - Extract and translate text from screenshots, photos, signs, etc.

## 🚨 Troubleshooting

### "Cannot connect to Ollama. Is it running?"
- Make sure Ollama is installed and running
- Check that Ollama is accessible at `http://localhost:11434`
- Try running `ollama serve` in your terminal

### Model Not Installed
- The application will show a "Download" button
- Click it to automatically download the selected model
- Or manually run: `ollama pull translategemma:27b`

### Translation Quality Issues
- Try using a larger model (27B > 12B > 4B)
- Ensure your source language is correctly selected
- For better results, use clear, well-formatted text

### Image Translation Not Working
- Ensure you're using a vision-capable model (all translateGemma models support this)
- Check that the image text is clear and readable
- Try with higher resolution images

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📜 License

This project uses:
- **translateGemma** - [Gemma Terms of Use](https://ai.google.dev/gemma/terms)
- **Ollama** - [Apache 2.0 License](https://github.com/ollama/ollama/blob/main/LICENSE)

## 🙏 Acknowledgments

- **Google** for the translateGemma model
- **Ollama** for the local LLM runtime
- **pdf.js** and **mammoth.js** for document processing

## 📞 Contact

Created by [Dwain-Barnes](https://github.com/Dwain-Barnes)

---

**Note**: This is a local-only application. No telemetry, no tracking, no cloud services. Your privacy is guaranteed.

## ⭐ Star This Project

If you find this useful, please give it a star on GitHub!
