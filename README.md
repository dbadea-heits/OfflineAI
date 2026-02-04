# OfflineAI 🤖

> An offline-first AI-powered mobile app using small language models (SLMs)

[![React Native](https://img.shields.io/badge/React%20Native-0.83.1-blue.svg)](https://reactnative.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-blue.svg)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## 📱 Overview

**OfflineAI** is a React Native mobile application that brings the power of AI language models directly to your device. With a focus on privacy and offline functionality, this app runs small language models (SLMs) locally on your phone, ensuring your conversations stay private and work without an internet connection.

### ✨ Key Features

- 🔒 **Privacy-First**: All AI processing happens on-device - your data never leaves your phone
- 📵 **Fully Offline**: No internet connection required after initial setup
- 🚀 **Fast & Responsive**: Optimized for mobile performance with efficient model inference
- 💬 **Conversational Context**: Maintains conversation history for coherent multi-turn dialogues
- 🎨 **Beautiful UI**: Modern, intuitive interface with markdown support for rich message formatting
- 📦 **Model Management**: Easy model selection and loading from local storage
- 💾 **Persistent Storage**: Conversations and settings saved locally using MMKV

## 🏗️ Architecture

### Tech Stack

- **Framework**: React Native 0.83.1
- **Language**: TypeScript 5.8.3
- **State Management**: Redux Toolkit
- **AI Engine**: [llama.rn](https://github.com/mybigday/llama.rn) - On-device LLM inference
- **Storage**: 
  - MMKV for fast key-value storage
  - SQLite for structured data
- **UI Components**:
  - React Native Markdown Display for rich text rendering
  - Custom components for chat interface

### Project Structure

```
OfflineAI/
├── src/
│   ├── components/       # Reusable UI components
│   │   ├── ChatInput.tsx
│   │   ├── MessageBubble.tsx
│   │   └── ModelSelector.tsx
│   ├── screens/          # App screens
│   │   └── ChatScreen.tsx
│   ├── store/            # Redux state management
│   │   ├── index.ts
│   │   └── chatSlice.ts
│   ├── hooks/            # Custom React hooks
│   ├── services/         # Business logic & API services
│   ├── db/               # Database & storage utilities
│   ├── utils/            # Helper functions & utilities
│   │   └── promptTemplates.ts
│   └── constants/        # App constants
├── models/               # Local AI models storage
├── ios/                  # iOS native code
├── android/              # Android native code
└── App.tsx              # App entry point
```

### Prompt Templates

The app supports multiple prompt formats for different model types:

- **ChatML**: Default format for Llama 3 and TinyLlama models
- **Alpaca**: Alternative format for Alpaca-based models

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have:

- **Node.js** >= 20
- **React Native development environment** set up ([Setup Guide](https://reactnative.dev/docs/set-up-your-environment))
- **Xcode** (for iOS development)
- **Android Studio** (for Android development)

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/dbadea-heits/OfflineAI.git
cd OfflineAI
```

2. **Install dependencies**

```bash
npm install
```

3. **Install iOS dependencies** (iOS only)

```bash
# Install Ruby bundler (first time only)
bundle install

# Install CocoaPods dependencies
cd ios
bundle exec pod install
cd ..
```

4. **Add AI models**

Place your GGUF model files in the `models/` directory. Compatible models include:
- TinyLlama
- Llama 3
- Phi-2
- Other GGUF format models

### Running the App

#### Start Metro Bundler

```bash
npm start
```

#### Run on iOS

```bash
npm run ios
```

#### Run on Android

```bash
npm run android
```

## 📖 Usage

1. **Select a Model**: On first launch, use the model selector to choose an AI model
2. **Start Chatting**: Type your message in the input field and press send
3. **View Responses**: AI responses are rendered with markdown support
4. **Continue Conversations**: The app maintains context across multiple messages

## 🛠️ Development

### Available Scripts

- `npm start` - Start Metro bundler
- `npm run ios` - Run on iOS simulator
- `npm run android` - Run on Android emulator
- `npm test` - Run tests
- `npm run lint` - Lint code with ESLint

### Code Style

This project uses:
- **ESLint** for code linting
- **Prettier** for code formatting
- **TypeScript** for type safety

## 🧪 Testing

```bash
npm test
```

## 📦 Building for Production

### iOS

```bash
# Build for iOS
cd ios
xcodebuild -workspace OfflineAI.xcworkspace -scheme OfflineAI -configuration Release
```

### Android

```bash
# Build APK
cd android
./gradlew assembleRelease
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [llama.rn](https://github.com/mybigday/llama.rn) - For making on-device LLM inference possible
- [React Native](https://reactnative.dev/) - For the amazing mobile framework
- The open-source AI community for developing small, efficient language models

## 📧 Contact

Dan Badea - [@dbadea-heits](https://github.com/dbadea-heits)

Project Link: [https://github.com/dbadea-heits/OfflineAI](https://github.com/dbadea-heits/OfflineAI)

---

**Built with ❤️ for privacy-conscious AI enthusiasts**
