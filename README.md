# 🚀 AI Resume & Application Assistant

[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?style=flat&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat&logo=react&logoColor=black)](https://reactjs.org/)
[![Groq](https://img.shields.io/badge/AI-Groq_Cloud-orange?style=flat)](https://groq.com/)

An intelligent full-stack solution that bridges the gap between a static resume and a personalized job application. By leveraging **Llama-3/Mixtral via Groq Cloud**, this tool parses complex PDF structures and generates tailored professional emails that align your specific experience with job requirements in seconds.

---

## ✨ Key Features

- **📄 Intelligent PDF Parsing**: Uses `pdfplumber` to handle multi-column layouts and extract clean text from complex resume structures.
- **🤖 LLM-Driven Tailoring**: Dynamically maps resume bullet points to job description keywords using high-speed inference from **Groq Cloud**.
- **⚡ Real-time Feedback**: Interactive UI with instant clipboard copying and visual upload confirmations.
- **🛡️ Privacy-Centric**: Resume processing is handled securely, ensuring sensitive data is extracted and structured before reaching the AI inference layer.
- **🎨 Modern UI**: A clean, minimalist interface built with React and Vite for optimal performance.

---

## 🧠 Tech Stack

| Layer               | Technology            | Role                                       |
| :------------------ | :-------------------- | :----------------------------------------- |
| **Frontend**        | React 18, Vite        | Single Page Application & State Management |
| **Backend**         | FastAPI (Python 3.9+) | Asynchronous API handling & PDF processing |
| **AI Inference**    | Groq Cloud API        | Llama-3 / Mixtral-8x7b LLM access          |
| **Data Extraction** | pdfplumber            | Deterministic PDF text extraction          |
| **Styling**         | Modern CSS            | Responsive, centered design                |

---

## 🏗️ System Architecture

1.  **Client-Side**: User uploads a `.pdf` resume and pastes a plain-text job description.
2.  **API Layer**: FastAPI receives the multipart form data; `pdfplumber` extracts the raw text.
3.  **Prompt Engineering**: The backend constructs a structured prompt containing the resume context and job requirements.
4.  **Inference**: Groq Cloud processes the prompt and returns a professionally formatted email.
5.  **Delivery**: The frontend renders the result with a one-click "Copy to Clipboard" feature.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- Node.js (v18+)
- A [Groq Cloud API Key](https://console.groq.com/)

### 1. Backend Configuration

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt

# Configure Environment
echo "GROQ_API_KEY=your_api_key_here" > .env

# Start Server
uvicorn main:app --reload
```

### 2. Frontend Configuration

```bash
cd frontend
npm install
npm run dev
```

---
