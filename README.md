# MindScribe: AI-Powered Mental Health Companion

![MindScribe Banner](https://placehold.co/1200x400/1E3A5F/FFFFFF?text=MindScribe%0AAI%20Mental%20Health%20Companion)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue.svg)
![React](https://img.shields.io/badge/React-18.3+-61DAFB.svg)
![WebLLM](https://img.shields.io/badge/WebLLM-Enabled-purple.svg)
![Whisper](https://img.shields.io/badge/Whisper-STT-green.svg)
![Piper](https://img.shields.io/badge/Piper-TTS-orange.svg)
[![Vercel](https://img.shields.io/badge/Vercel-Ready-black.svg)](https://vercel.com)

A comprehensive, privacy-first mental health support platform powered by local AI. MindScribe provides therapeutic conversations, voice therapy sessions, mood journaling with AI analysis, and personalized mental health insights — all running directly in your browser with zero data leaving your device.

## 🌟 What Makes MindScribe Special

- **🔒 100% Private:** All AI processing happens locally in your browser - no servers, no API calls
- **🧠 DASS-21 Assessment:** Clinically-validated mental health screening for personalized support
- **🎙️ Voice Therapy:** Speech-to-text (Whisper) and text-to-speech (Piper) for hands-free sessions
- **📓 Smart Journaling:** AI-powered mood analysis, sentiment detection, and emotion tracking
- **📊 Analytics Dashboard:** Visual insights into mood trends, stress levels, and emotional patterns
- **📄 Export Reports:** Generate PDF reports and export data in JSON/CSV formats
- **💻 Fully Offline:** Works without internet after initial model download

## ✨ Complete Feature Set (27 Features)

### 🔐 **Phase 1: Core Infrastructure**

| Feature                    | Description                                     |
| -------------------------- | ----------------------------------------------- |
| **F001** Auth System       | Local authentication with encrypted credentials |
| **F002** Encrypted Storage | AES-GCM encryption using Web Crypto API         |
| **F003** Theme System      | Dark/Light mode with system preference sync     |
| **F004** Layout System     | Responsive sidebar navigation with AppLayout    |

### 🧪 **Phase 2: Mental Health Assessment**

| Feature                     | Description                                 |
| --------------------------- | ------------------------------------------- |
| **F005** DASS-21 Assessment | Depression, Anxiety, Stress screening tool  |
| **F006** Assessment Results | Visual severity display with color coding   |
| **F007** User Onboarding    | First-time user flow with guided assessment |

### 💬 **Phase 3: AI Therapy Chat**

| Feature                    | Description                                |
| -------------------------- | ------------------------------------------ |
| **F008** WebLLM Chat       | Local AI conversations (Qwen2.5-0.5B/1.5B) |
| **F009** DASS-21 Context   | Personalized responses based on assessment |
| **F010** Chat History      | Persistent sessions with smart memory      |
| **F011** Typing Indicators | Real-time AI thinking animations           |

### 🎙️ **Phase 4: Voice Therapy**

| Feature                   | Description                                 |
| ------------------------- | ------------------------------------------- |
| **F012** Whisper STT      | Speech-to-text using Transformers.js        |
| **F013** Piper TTS        | Text-to-speech with 5 ASMR voices           |
| **F014** Voice Visualizer | Audio waveform animations                   |
| **F015** Voice Selector   | Choose from Amy, Aurora, Luna, Nova, Willow |
| **F016** Voice Session    | Push-to-talk therapy conversation flow      |

### 📓 **Phase 5: Journaling**

| Feature                  | Description                         |
| ------------------------ | ----------------------------------- |
| **F017** Journal Editor  | Rich text entry with auto-save      |
| **F018** AI Analysis     | Mood, sentiment, stress detection   |
| **F019** Journal History | Searchable entries with filters     |
| **F020** Entry Details   | Detailed analysis per journal entry |

### 📊 **Phase 6: Dashboard & Analytics**

| Feature                       | Description                         |
| ----------------------------- | ----------------------------------- |
| **F021** Stats Overview       | Total entries, average mood, trends |
| **F022** Mood Charts          | Area chart for sentiment over time  |
| **F023** Emotion Distribution | Pie chart for emotion breakdown     |
| **F024** Stress Levels        | Bar chart for stress patterns       |
| **F025** DASS-21 Progress     | Assessment baseline display         |

### 📄 **Phase 7: Reports & Export**

| Feature              | Description                              |
| -------------------- | ---------------------------------------- |
| **F026** PDF Reports | Generate comprehensive mental health PDF |
| **F027** Data Export | Export as JSON or CSV for backup         |

## 🏗️ Architecture

```
MindScribe/
├── src/
│   ├── components/
│   │   ├── auth/           # Authentication components
│   │   ├── chat/           # Chat interface & history
│   │   ├── layout/         # AppLayout, navigation
│   │   ├── navigation/     # Sidebar, model selector
│   │   └── ui/             # Shadcn/ui components
│   ├── contexts/
│   │   └── AuthContext.tsx # Authentication state
│   ├── hooks/
│   │   ├── use-chat.tsx    # Chat state management
│   │   ├── use-chat-session.ts # Session persistence
│   │   ├── use-voice.ts    # Voice therapy hook
│   │   └── use-persistent-chat.ts # Memory management
│   ├── pages/
│   │   ├── login.tsx       # Authentication
│   │   ├── assessment.tsx  # DASS-21 screening
│   │   ├── chat.tsx        # AI therapy chat
│   │   ├── voice.tsx       # Voice therapy
│   │   ├── journal.tsx     # Mood journaling
│   │   ├── dashboard.tsx   # Analytics dashboard
│   │   └── reports.tsx     # Export & reports
│   ├── services/
│   │   ├── auth-service.ts          # User authentication
│   │   ├── storage-service.ts       # Encrypted storage
│   │   ├── webllm-service.ts        # Local AI models
│   │   ├── voice-service.ts         # Whisper STT + Piper TTS
│   │   ├── journal-service.ts       # Journal management
│   │   ├── chat-memory-service.ts   # Session persistence
│   │   ├── mental-health-prompt-service.ts # DASS-21 prompts
│   │   └── report-service.ts        # PDF/JSON/CSV export
│   └── types/
│       └── schema.ts       # TypeScript definitions
├── public/
│   └── wasm/               # ONNX & Piper WASM files
└── vite.config.ts
```

## 🛠️ Tech Stack

| Category           | Technology                                   |
| ------------------ | -------------------------------------------- |
| **Frontend**       | React 18.3, TypeScript 5.0, Vite 5.4         |
| **Styling**        | Tailwind CSS, Shadcn/ui, Framer Motion       |
| **AI Chat**        | WebLLM (Qwen2.5-0.5B-Instruct, Qwen2.5-1.5B) |
| **Speech-to-Text** | Whisper Tiny EN (Transformers.js, q8)        |
| **Text-to-Speech** | Piper WASM + espeak-ng phonemizer            |
| **Storage**        | LocalForage + Web Crypto API (AES-GCM)       |
| **Charts**         | Recharts (Area, Bar, Pie, Line charts)       |
| **PDF Export**     | jsPDF + jspdf-autotable                      |
| **Deployment**     | Vercel, Netlify, GitHub Pages                |

## 🚀 Quick Start

### Option 1: Deploy to Vercel (Recommended)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/ErDashrath/EchoLearn)

### Option 2: Local Development

```bash
# Clone the repository
git clone https://github.com/ErDashrath/EchoLearn.git
cd EchoLearn

# Install dependencies
npm install

# Start development server
npm run dev

# Open in browser
# http://localhost:5173
```

### Option 3: Production Build

```bash
# Build for production
npm run build

# Preview production build
npm run preview
```

## 📱 Browser Compatibility

| Browser           | Support | WebGPU | Voice  | Performance |
| ----------------- | ------- | ------ | ------ | ----------- |
| **Chrome 113+**   | ✅ Full | ✅ Yes | ✅ Yes | ⭐⭐⭐⭐⭐  |
| **Edge 113+**     | ✅ Full | ✅ Yes | ✅ Yes | ⭐⭐⭐⭐⭐  |
| **Firefox 110+**  | ✅ Full | ⚠️ CPU | ✅ Yes | ⭐⭐⭐⭐    |
| **Safari 16.4+**  | ✅ Full | ⚠️ CPU | ✅ Yes | ⭐⭐⭐      |
| **Mobile Chrome** | ✅ Full | ✅ Yes | ✅ Yes | ⭐⭐⭐⭐    |

## 🎯 How to Use

### 1. **Create Account & Login**

- Register with username and password
- Credentials are encrypted and stored locally
- No email verification required

### 2. **Complete DASS-21 Assessment**

- 21-question mental health screening
- Measures Depression, Anxiety, and Stress
- Results personalize your AI companion

### 3. **Chat with AI Therapist**

- Open the Chat page from sidebar
- Download and activate an AI model
- Start conversations with personalized support

### 4. **Voice Therapy Sessions**

- Navigate to Voice Therapy page
- Select your preferred ASMR voice
- Hold the microphone button to speak
- AI responds with soothing voice

### 5. **Daily Journaling**

- Write your thoughts and feelings
- AI analyzes mood, sentiment, and emotions
- Track patterns over time

### 6. **View Dashboard**

- See mood trends and statistics
- Emotion distribution charts
- Stress level patterns
- DASS-21 baseline comparison

### 7. **Export Reports**

- Generate PDF mental health summary
- Export data as JSON for backup
- Export journal entries as CSV

## 🎙️ Voice Therapy Voices

| Voice      | Style             | Best For           |
| ---------- | ----------------- | ------------------ |
| **Amy**    | Warm, nurturing   | General support    |
| **Aurora** | Gentle, calming   | Anxiety relief     |
| **Luna**   | Soft, soothing    | Sleep & relaxation |
| **Nova**   | Clear, reassuring | Guided exercises   |
| **Willow** | Whispery, ASMR    | Deep relaxation    |

## 🔧 Available AI Models

| Model            | Size  | Speed  | Quality  | Memory |
| ---------------- | ----- | ------ | -------- | ------ |
| **Qwen2.5-0.5B** | 500MB | ⚡⚡⚡ | ⭐⭐⭐   | 2GB    |
| **Qwen2.5-1.5B** | 1.5GB | ⚡⚡   | ⭐⭐⭐⭐ | 4GB    |
| **Llama 3.2 1B** | 1.2GB | ⚡⚡⚡ | ⭐⭐⭐   | 3GB    |
| **Llama 3.2 3B** | 2.0GB | ⚡⚡   | ⭐⭐⭐⭐ | 6GB    |

## 🔒 Privacy & Security

MindScribe is built with privacy as the core principle:

- **🚫 No Data Collection:** Zero telemetry, no analytics, no tracking
- **🔐 Local Encryption:** AES-GCM encryption for all stored data
- **💻 Browser-Only:** All AI runs in your browser via WebGPU/WASM
- **📵 Fully Offline:** Works without internet after setup
- **🗑️ Your Control:** Delete all data anytime from settings

## 📊 DASS-21 Severity Levels

| Score Range          | Depression | Anxiety | Stress |
| -------------------- | ---------- | ------- | ------ |
| **Normal**           | 0-9        | 0-7     | 0-14   |
| **Mild**             | 10-13      | 8-9     | 15-18  |
| **Moderate**         | 14-20      | 10-14   | 19-25  |
| **Severe**           | 21-27      | 15-19   | 26-33  |
| **Extremely Severe** | 28+        | 20+     | 34+    |

## 🛠️ Development

### Available Scripts

```bash
npm run dev        # Start development server
npm run build      # Build for production
npm run preview    # Preview production build
npm run lint       # Run ESLint
npx tsc --noEmit   # TypeScript type checking
```

### Project Structure

```
src/
├── components/    # Reusable UI components
├── contexts/      # React context providers
├── hooks/         # Custom React hooks
├── pages/         # Application pages
├── services/      # Business logic & APIs
└── types/         # TypeScript definitions
```

## 🐛 Troubleshooting

### **AI Model Won't Load**

- Ensure WebGPU is enabled in browser
- Try a smaller model (Qwen2.5-0.5B)
- Check available memory (4GB+ recommended)

### **Voice Not Working**

- Allow microphone permissions
- Check browser audio settings
- Voice models download on first use (~20MB)

### **Slow Performance**

- Use Chrome/Edge for best WebGPU support
- Close other memory-heavy tabs
- Use smaller AI model

### **Data Not Saving**

- Check localStorage availability
- Clear browser cache and retry
- Ensure cookies are enabled

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## ⚠️ Disclaimer

MindScribe is an AI-powered wellness tool and **NOT a substitute for professional mental health care**. If you're experiencing a mental health crisis, please contact:

- **National Suicide Prevention Lifeline:** 988 (US)
- **Crisis Text Line:** Text HOME to 741741
- **International Association for Suicide Prevention:** https://www.iasp.info/resources/Crisis_Centres/

## 🙏 Acknowledgments

- **WebLLM** - Browser-based LLM inference
- **Transformers.js** - Whisper speech recognition
- **Piper** - Neural text-to-speech
- **Shadcn/ui** - Beautiful UI components
- **Recharts** - Data visualization
- **jsPDF** - PDF generation

---

<div align="center">

**Built with ❤️ for Mental Wellness by [Saniya](https://github.com/sanudii24/MindScribe)**

[⭐ Star this repo](https://github.com/ErDashrath/EchoLearn) | [🐛 Report Bug](https://github.com/ErDashrath/EchoLearn/issues) | [💡 Request Feature](https://github.com/ErDashrath/EchoLearn/issues)

</div>
