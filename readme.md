# 🦙 Ollama Chat Interface - Beautiful Web UI for Local AI Models

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Ollama](https://img.shields.io/badge/Ollama-Compatible-blue)](https://ollama.ai/)

A **modern, responsive web interface** for chatting with local AI models through Ollama. Features real-time streaming responses, mathematical expression rendering, and a beautiful glassmorphism design.

## 🌟 Features

### ✨ **Modern Design**
- **Glassmorphism UI** with gradient backgrounds
- **Responsive design** works on desktop, tablet, and mobile
- **Dark/Light themed** message bubbles
- **Smooth animations** and transitions
- **Mobile-optimized** touch interface

### 🤖 **AI Chat Features**
- **Real-time streaming** responses from Ollama models
- **Model selection** dropdown with automatic detection
- **Formatted responses** with proper rendering for:
  - Mathematical expressions (`\( \)`, `\[ \]`, `$ $`, `$$ $$`)
  - Code blocks with syntax highlighting
  - **Think tags** with special formatting
  - **Boxed answers** for highlighted results
  - Bold, italic, and structured text

### 🚀 **Technical Features**
- **No dependencies** - Pure HTML, CSS, JavaScript
- **CORS handling** with clear error messages
- **Auto-scroll** to latest messages
- **Keyboard shortcuts** (Enter to send)
- **Connection status** indicator
- **Error handling** with user-friendly messages

## 🛠️ Quick Start

### Prerequisites
- [Ollama](https://ollama.ai/) installed and running
- At least one AI model downloaded (e.g., `ollama pull llama2`)
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Installation

1. **Download the HTML file**
   ```bash
   curl -O https://raw.githubusercontent.com/yourusername/ollama-chat-interface/main/ollama-chat.html
   ```

2. **Start Ollama with CORS enabled**
   
   **Windows (PowerShell):**
   ```powershell
   $env:OLLAMA_ORIGINS="*"
   ollama serve
   ```
   
   **Linux/macOS:**
   ```bash
   OLLAMA_ORIGINS=* ollama serve
   ```
   
   **Command Prompt (Windows):**
   ```cmd
   set OLLAMA_ORIGINS=*
   ollama serve
   ```

3. **Open the HTML file** in your web browser

4. **Start chatting!** 🎉

## 📱 Usage

### Basic Chat
1. **Select a model** from the dropdown menu
2. **Type your message** in the input field
3. **Press Enter** or click the send button
4. **Watch responses stream** in real-time

### Advanced Features

#### Mathematical Expressions
The interface automatically formats mathematical content:

```
Input: What is 8 + 999?
Output: Properly formatted with \( 8 + 999 = 1007 \) and \boxed{1007}
```

#### Code Discussions
Code blocks are automatically highlighted:

```python
def hello_world():
    print("Hello from Ollama!")
```

#### Thinking Process
Models that output `<think>` tags will show formatted thinking sections.

## 🔧 Configuration

### Environment Variables

| Variable | Description | Default | Example |
|----------|-------------|---------|---------|
| `OLLAMA_ORIGINS` | CORS origins | `localhost` | `*` or `http://localhost:3000` |
| `OLLAMA_HOST` | Ollama server host | `localhost:11434` | `0.0.0.0:11434` |

### Customization

#### Modify Ollama URL
Edit the `OLLAMA_URL` constant in the HTML file:
```javascript
const OLLAMA_URL = 'http://your-ollama-server:11434';
```

#### Styling
The interface uses CSS custom properties for easy theming:
```css
:root {
  --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  --message-bg: #f1f3f4;
  --accent-color: #667eea;
}
```

## 🐛 Troubleshooting

### Common Issues

#### ❌ **403 Forbidden / CORS Error**
**Solution:** Start Ollama with CORS enabled:
```bash
OLLAMA_ORIGINS=* ollama serve
```

#### ❌ **Connection Failed**
**Solutions:**
1. Verify Ollama is running: `curl http://localhost:11434/api/tags`
2. Check firewall settings
3. Ensure correct port (default: 11434)

#### ❌ **No Models Found**
**Solutions:**
1. Download models: `ollama pull llama2`
2. Verify models: `ollama list`
3. Restart Ollama service

#### ❌ **Slow Responses**
**Solutions:**
1. Use smaller models (7B instead of 70B)
2. Increase system RAM allocation
3. Use GPU acceleration if available

### Debug Mode
Open browser Developer Tools (F12) to see detailed error messages and network requests.

## 🚀 Performance Optimization

### Recommended Models
- **Fast responses:** `llama2:7b`, `mistral:7b`
- **Better quality:** `llama2:13b`, `codellama:13b`
- **Specialized:** `codellama:python`, `vicuna:7b`

### System Requirements
| Model Size | RAM Required | Response Time |
|------------|--------------|---------------|
| 7B | 8GB+ | ~2-5 seconds |
| 13B | 16GB+ | ~5-10 seconds |
| 70B | 64GB+ | ~15-30 seconds |

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Development Setup
1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes
4. Test with multiple models
5. Submit a pull request

### Areas for Contribution
- [ ] **Themes:** Additional color schemes
- [ ] **Features:** File upload support
- [ ] **Models:** Model parameter controls
- [ ] **Export:** Chat history export
- [ ] **Voice:** Speech-to-text integration
- [ ] **Mobile:** PWA functionality

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **[Ollama Team](https://ollama.ai/)** - For the amazing local AI platform
- **Community Contributors** - For feedback and improvements
- **Open Source Community** - For inspiration and tools

## 📊 Project Stats

- **Lines of Code:** ~500 HTML/CSS/JS
- **Dependencies:** Zero external dependencies
- **Browser Support:** All modern browsers
- **Mobile Ready:** Fully responsive design
- **Performance:** Real-time streaming responses

## 🔗 Related Projects

- [Ollama](https://ollama.ai/) - Run large language models locally
- [Open WebUI](https://github.com/open-webui/open-webui) - Advanced Ollama web interface
- [Ollama Python](https://github.com/ollama/ollama-python) - Python client for Ollama
- [Ollama JS](https://github.com/ollama/ollama-js) - JavaScript client for Ollama

## 📞 Support

- **Issues:** [GitHub Issues](https://github.com/yourusername/ollama-chat-interface/issues)
- **Discussions:** [GitHub Discussions](https://github.com/yourusername/ollama-chat-interface/discussions)
- **Ollama Support:** [Ollama Documentation](https://github.com/ollama/ollama)

---

⭐ **Star this repo** if you find it helpful! It helps others discover the project.

**Keywords:** ollama, ai chat, local ai, llama2, mistral, web interface, html5, javascript, responsive design, real-time streaming, mathematical expressions, code highlighting, glassmorphism ui, cors, open source