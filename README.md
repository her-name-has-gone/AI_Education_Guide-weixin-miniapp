# Indievolve - AI Education Assistant (WeChat Mini Program)

Indievolve (小树AI助教) is an AI-powered education assistant designed for teachers. It provides features like lesson planning, question generation, and personalized feedback generation using advanced LLMs (Claude, Gemini, Grok).

## 🚀 Features

*   **AI Lesson Planning**: Generate structured lesson plans based on subject and grade.
*   **Question Generation**: Create quiz questions and exercises automatically.
*   **Student Feedback**: Generate personalized comments and assessments for students.
*   **Multi-modal Support**: Supports text and image inputs (e.g., OCR for analyzing handwritten work).

## 🛠️ Technology Stack

*   **Frontend**: Native WeChat Mini Program + UniApp Components
*   **Backend Proxy**: Node.js (Express)
*   **AI Integration**: OpenRouter API (Claude 3.5 Sonnet, etc.)

## ⚙️ Setup & Installation

### 1. Prerequisites
*   Node.js (v14+)
*   WeChat Developer Tools

### 2. Configuration (Important!)
This project uses sensitive API keys that are **not** tracked in git. You must create a local configuration file.

1.  Navigate to `config/` directory.
2.  Copy `api.example.js` to `api.js`.
    ```bash
    cp config/api.example.js config/api.js
    ```
3.  Edit `config/api.js` and fill in your real API keys (Claude, Gemini, etc.).

> **Note**: `config/api.js` is added to `.gitignore` to prevent accidental commits of secrets.

### 3. Backend Server
The mini program relies on a local proxy server to communicate with LLM APIs.

```bash
# Install dependencies
npm install

# Start the server
node server_new.js
```
The server will run on `http://localhost:9100`.

### 4. Running the Mini Program
1.  Open **WeChat Developer Tools**.
2.  Import this project directory (`e:\indievolve\mp-weixin`).
3.  Ensure the "AppID" matches your configuration (or use Test ID).
4.  Compile and run.

## 📂 Project Structure

*   `pages/`: Frontend pages (Home, Scene Detail, etc.)
*   `server_new.js`: Backend proxy server
*   `config/`: Configuration files (API keys)
*   `services/`: LLM service wrappers
*   `cloudfunctions/`: WeChat Cloud Functions (optional)

## 🤝 Contributing

1.  Ensure you do **not** commit `config/api.js`.
2.  Follow the commit message convention: `type: description` (e.g., `feat: add new scene`).

## 📄 License
Private (Indievolve Team)
