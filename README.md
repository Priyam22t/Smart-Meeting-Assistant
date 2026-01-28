# 🧠 Smart Meeting Assistant

Smart Meeting Assistant is an AI-powered application that enhances online meetings by providing real-time transcription, silent monitoring, and contextual question answering. The assistant listens passively during meetings and only responds when explicitly invoked with “Hey Assistant”, ensuring a non-intrusive and focused meeting experience.

---

## 🚀 Features

- 🎙️ Real-time speech transcription  
- 🤖 AI-powered contextual Q&A  
- 🔕 Completely silent unless explicitly invoked  
- 📊 Meeting transcript and summary generation  
- 🎥 Live video call integration using Stream  
- 🧠 Gemini-powered real-time AI responses  

---

## 🏗️ Project Structure

Smart-Meeting-Assistant/  
├── backend/  
│   ├── .venv/                # Python virtual environment  
│   ├── main.py               # Backend agent logic  
│   ├── pyproject.toml        # Python dependencies  
│   ├── .env                  # Environment variables  
│  
├── meeting-assistant/        # Frontend (Next.js)  
│   ├── app/  
│   ├── components/  
│   ├── hooks/  
│   ├── meeting/[id]/page.jsx # Meeting room UI  
│   └── ...  
│  
└── README.md  

---

## 🛠️ Tech Stack

Backend  
- Python 3.12  
- Vision Agents  
- Stream Video SDK  
- Gemini Realtime LLM  
- asyncio  
- python-dotenv  
- websockets  

Frontend  
- Next.js (App Router)  
- React  
- Stream Video React SDK  
- Tailwind CSS  

---

## 🔐 Environment Variables

Create a `.env` file inside the backend folder:

STREAM_API_KEY=your_stream_api_key  
STREAM_API_SECRET=your_stream_api_secret  
CALL_ID=demo-meeting-room  

---

## ⚙️ Backend Setup

1. Navigate to backend  
cd backend  

2. Create virtual environment  
py -3.12 -m venv .venv  

3. Activate virtual environment (Windows)  
.venv\Scripts\activate.bat  

4. Install dependencies  
python -m pip install --upgrade pip  
python -m pip install python-dotenv  
python -m pip install "vision-agents[deepgram,gemini,getstream]"  
python -m pip install websockets  

5. Run backend  
python main.py  

---

## 🖥️ Frontend Setup

1. Navigate to frontend  
cd meeting-assistant  

2. Install dependencies  
npm install  

3. Run frontend  
npm run dev  

Open browser at:  
http://localhost:3000  

---

## 🧠 How It Works

1. A meeting starts via a Stream video call  
2. The assistant silently listens and transcribes speech  
3. Transcripts are stored in memory during the session  
4. When someone says “Hey Assistant”, the AI:  
   - Extracts the question  
   - Uses the meeting transcript as context  
   - Responds concisely using Gemini  
5. When the meeting ends, a full transcript summary is generated  

---

## 📌 Example Usage

User: Hey Assistant, summarize the meeting  
Assistant: Provides a concise summary based on the conversation  

User: Hey Assistant, what are the action items?  
Assistant: Lists action items discussed during the meeting  

---

## ⚠️ Assistant Rules

- Never speaks unless explicitly invoked  
- Never interrupts participants  
- Never responds to side conversations  
- Responds only to “Hey Assistant + question”  

---

## 📈 Future Improvements

- Persistent transcript storage (database)  
- Speaker identification  
- Automatic action item extraction  
- Multi-language transcription  
- Calendar and email integrations  

---

## 👨‍💻 Author

Built as an advanced AI and real-time systems project to explore LLM orchestration, real-time media pipelines, and event-driven AI agents.

---

## 📜 License

This project is intended for educational and experimental purposes.
