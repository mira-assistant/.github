# Mira Assistant

Mira is a sophisticated AI-powered personal assistant that combines real-time voice interaction, custom-trained language models, and a modern desktop interface. Built with a focus on privacy, performance, and extensibility, Mira represents a complete end-to-end solution for voice-based AI interaction.

## 🌟 Key Features

- **Real-time Voice Interaction**: Powered by Whisper Live technology for instant speech-to-text conversion
- **Custom-trained AI Models**: Two specialized language models fine-tuned for specific tasks
- **Cross-platform Desktop Client**: Modern Electron-based interface for macOS and Windows
- **Secure Network Architecture**: Private deployment using Tailscale for device connectivity
- **Extensible Backend**: FastAPI-based Python backend with modular architecture
- **Comprehensive Testing**: 67+ tests across all components

## 🧠 AI Models

### 1. Command Processing Model (LLaMA-2-7B-Chat)
- Fine-tuned version of LLaMA-2-7B-Chat optimized for:
  - Natural language command interpretation
  - Wake word response handling
  - Function calling and system control
- Utilizes LoRA (Low-Rank Adaptation) for efficient training
- Optimized for real-time response generation

### 2. Data Extraction Model (Falcon-40B-Instruct)
- Custom-tuned version of TII UAE Falcon-40B-Instruct for:
  - Structured data extraction from speech
  - Contact information parsing
  - Calendar event recognition
  - Task and reminder extraction
- Enhanced with task-specific prompts and examples
- Optimized for accuracy in entity extraction

## 🔧 Technical Architecture

### Backend (Python/FastAPI)
- **Core Components**:
  - FastAPI application server
  - SQLite database with SQLAlchemy ORM
  - Custom ML model manager
  - Real-time audio processing pipeline
  
- **API Routes**:
  ```
  /interactions
  ├── POST /register          # Register new voice interactions
  ├── GET /{id}              # Retrieve specific interactions
  ├── POST /{id}/inference   # Run inference on interaction
  └── DELETE /{id}           # Remove interaction
  
  /conversations
  └── GET /all               # Retrieve conversation history
  
  /persons
  └── [Person management endpoints]
  
  /services
  └── [System service endpoints]
  
  /streams
  └── [Real-time stream management]
  ```

### Desktop Client (Electron/Node.js)
- Modern UI with intuitive design
- Real-time voice capture and streaming
- Secure IPC bridge architecture
- Professional animations and visual feedback
- Keyboard shortcuts for efficiency

## 🚀 Installation

### Backend Setup
```bash
# Clone the repository
git clone https://github.com/your-org/mira-assistant.git
cd mira-assistant/backend

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start the server
python mira.py
```

### Desktop Client Setup
```bash
# Navigate to desktop client
cd ../desktop-client

# Install dependencies
npm install

# Start the application
npm start

# For development mode
npm run start-dev
```

## 🔒 Secure Deployment with Tailscale

Mira uses Tailscale for secure, private networking between devices:

1. **Network Setup**:
   - Install Tailscale on all devices
   - Create a private Tailscale network
   - Configure subnet routing for local services

2. **Backend Configuration**:
   - Deploy backend on primary device
   - Expose backend port through Tailscale network
   - Configure client to use Tailscale IP

3. **Client Configuration**:
   - Update `baseUrl` in client config to use Tailscale IP
   - Enable secure WebSocket connections
   - Maintain end-to-end encryption

## 🧪 Testing

```bash
# Backend Tests
cd backend
python -m pytest tests/

# Desktop Client Tests
cd desktop-client
npm test
```

## 🛠 Development

### Model Fine-tuning
```bash
cd backend/tuning

# Generate training datasets
python acquire_datasets.py --task both --output-dir datasets/

# Fine-tune models
python fine_tune_models.py --model llama-2-7b-chat-hf-function-calling-v3
python fine_tune_models.py --model tiiuae-falcon-40b-instruct
```

### Building for Distribution
```bash
cd desktop-client

# Build for macOS
npm run build-mac

# Build for Windows
npm run build-win

# Build for all platforms
npm run build
```

## 📚 Technical Stack

- **Backend**:
  - Python 3.8+
  - FastAPI
  - SQLAlchemy
  - PyTorch
  - Transformers
  - Whisper Live

- **Frontend**:
  - Electron
  - Node.js
  - Modern JavaScript (ES6+)
  - HTML5/CSS3
  - Web Audio API

- **ML/AI**:
  - LLaMA-2-7B-Chat
  - Falcon-40B-Instruct
  - LoRA fine-tuning
  - Custom training pipelines

- **Deployment**:
  - Tailscale
  - SQLite
  - LM Studio
  - Electron Builder

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- The LLaMA team at Meta AI Research
- The Falcon team at Technology Innovation Institute
- The Whisper team at OpenAI
- The Tailscale team for their excellent networking solution
