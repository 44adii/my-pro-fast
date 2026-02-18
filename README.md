# ⚖️ NyayaGPT - AI Legal Assistant

**NyayaGPT** is a next-generation AI Legal Assistant designed to simplify legal access for everyone. It uses **Google Gemini 2.5 Flash Lite** and a **CrewAI Multi-Agent System** to listen to legal problems, classify them, identify relevant Indian Penal Code (IPC) sections, retrieve precedent cases, and automatically draft official legal documents like FIRs.

## 🚀 Key Features

*   **📝 Plain English Input**: Describe your legal issue in your own words.
*   **🎙️ Voice-First Interface**: Speak your problem efficiently. Uses **Faster-Whisper** for high-accuracy local transcription (Hindi/English support).
*   **🤖 Multi-Agent AI Workflow**: Specialized agents extract facts, identify IPC sections, retrieve case law, and generate documents.
    *   **Case Intake Agent**: Structures raw unstructured user stories.
    *   **Advisory Agent**: Determines if a case is Civil/Criminal and advises the immediate next step (e.g., "File FIR").
    *   **Legal Drafter Agent**: Writes **Standard Official Legal Letters** (To The SHO/Court Format) instead of generic AI text.
*   **📚 Retrieval-Augmented Generation (RAG)**: Combines semantic search with generative AI for accurate, grounded responses.
*   **🧠 Precedent Search**: Finds relevant judicial precedents for your scenario using semantic search.
*   **📄 Professional Tools**:
    *   **PDF Generation**: Instantly download drafted legal documents as formatted PDFs (`jspdf`).
    *   **Lawyer Connect**: One-click "Email to Lawyer" feature to send drafts to legal professionals.
*   **🔐 Dual-Mode Authentication**:
    *   **Phone Login**: Sign in instantly using a mobile number.
    *   **Email Login**: Standard email/password authentication.
*   **⚡ Modern Stack**: Built with **React + Vite** (Frontend) and **FastAPI** (Backend) for blazing fast performance.

---

## 🛠️ Tech Stack

*   **Frontend**: React, TailwindCSS, Lucide Icons, jsPDF
*   **Backend**: FastAPI, Uvicorn, Python 3.12
*   **AI Core**: CrewAI (Agent Orchestration), Google Gemini 2.5 Flash Lite (LLM), Faster-Whisper (ASR)
*   **Database**: MongoDB (User Data), ChromaDB/FAISS (Vector Search for RAG)
*   **Deployment**: Ready for local hosting or cloud deployment.

---

## 📦 Installation & Setup

### 1. Clone the Repo
```bash
git clone https://github.com/44adii/my-pro-fast.git
cd my-pro-fast
```

### 2. Backend Setup
```bash
cd backend
pip install -r requirements.txt

# Create .env file with your API Key and Configs
echo "GOOGLE_API_KEY=your_key_here" > .env
echo "MONGO_URI=mongodb://localhost:27017" >> .env

# Run Server
python main.py
# OR
uvicorn main:app --reload --port 8001
```

### 3. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

### 4. Usage
*   Open `http://localhost:5173`.
*   **Login** using Phone or Email.
*   Click the **microphone** to speak your legal issue OR type it in the text area.
*   Click **"Analyze"** to get a structured legal strategy, IPC sections, and advice.
*   Click **"Date & Draft"** to generate and download a formal legal application (PDF).

---

## 🧩 Agentic AI & RAG

- **Agentic AI:** The backend uses **CrewAI** to orchestrate multiple specialized agents.
    - *Intake Agent* -> *Advisory Agent* -> *IPC Agent* -> *Precedent Agent* -> *Drafing Agent*.
- **RAG (Retrieval-Augmented Generation):** The system retrieves relevant legal sections and case law from a vector database, then uses this information to generate accurate, context-aware responses, reducing hallucinations.

---

## ⚠️ Disclaimer

> This tool is for informational purposes only and **does not constitute legal advice**. For professional legal counsel, please consult a qualified attorney.

---

## 🛡️ License

MIT License. Free to use for educational and legal aid innovation.
