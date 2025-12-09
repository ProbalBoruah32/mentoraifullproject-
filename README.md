🌟 MentorAI: 

AI-Powered Communication Assessment Ecosystem 🗣️
A Complete End-to-End Platform for Real-Time Speech Analysis, Intelligent Scoring, and Skill Improvement
🛡️ Project Status & Technology Stack
Category	Status	Tech Used
Project Status	✔️ Active	—
Backend	✔️ Node.js, HuggingFace	Whisper ASR
AI / ML	✔️ Integrated	Whisper + Scoring Engine
Frontend / Mobile	✔️ Web App + Android	Kotlin + JNI
🗺️ Table of Contents

🌟 MentorAI Overview

🚀 Core Features & User Benefits

🧱 System Architecture & Data Flow

💻 Technology Stack

⚙️ Backend Setup (mentorai-backend)

☁️ Deploy Backend on Hugging Face

🌐 Web Application Setup

📱 Android Application Guide

🎬 Demonstration Videos & Screenshot Slots

🤝 Credits

📄 Technical Documentation Slot

🌟 MentorAI Overview: A Communication Revolution

MentorAI is a fully integrated, AI-powered communication assistant built to evaluate and dramatically improve speaking skills.
It moves beyond simple transcription by offering deep linguistic analysis, intelligent scoring, and interactive learning tools.

Our mission is to combine:

advanced AI

real-time processing

intelligent feedback

cross-platform deployment

…into a single ecosystem that empowers people to master communication.

🧠 What is MentorAI?

MentorAI is an AI-driven communication assessment platform built to analyze and score speaking proficiency.

It includes:

🎤 Real-time Microphone Transcription
🤖 Whisper ASR (Speech-to-Text)
🧮 AI-based Scoring Engine (0–10 scale)
📱 Android App with WebView + JNI URL Protection
🌐 Fully Hosted Backend on HuggingFace

🚀 Core Features & User Benefits
✅ Evaluation Features
Feature	Description
Segment-by-Segment Scoring	Breaks long audio/video into parts and scores each individually.
AI Scoring Engine	Computes fluency, clarity, pace, pronunciation.
Audio/Video Upload Evaluation	Accepts recorded files for deep analysis.
Translation Support	Helps practice multilingual communication.
Whisper ASR Integration	Ultra-accurate transcription engine.
🎯 User Benefits
Benefit	Focus
✔ Practice Speaking	Interactive, real-time improvement.
✔ Improve Pronunciation	Analyze phonetic accuracy.
✔ Boost Fluency	Pace and pause detection.
✔ Track Progress	Numerical scoring over time.
✔ Guided Feedback	Actionable suggestions for improvement.
🧱 System Architecture & Data Flow

MentorAI’s architecture is modular, flexible, and interconnected.

📁 Project Structure

MentorAI /

 ├── mentorai-backend/           # Node.js backend + Whisper ASR + AI scoring engine
 
 ├── mentoraiapplicationwork/    # Frontend scoring interface & audio/video workflow
 
 └── android-app/                # Secure Android app using WebView + JNI

🏗️ Architecture Diagram 


<img width="1536" height="1024" alt="40f591b5-bf63-4bc2-b369-bff421166937" src="https://github.com/user-attachments/assets/71c46094-a03a-4dc8-bc81-0a3539df8f2c" />


🔄 Data Flow Diagram 
graph TD

    A[👤 User] -->|1. Speaks / Uploads| B(📱 Android App / 🌐 Web Frontend)
    
    B -->|2. API Call (HTTPS)| C(☁️ Hugging Face Space)
    
    C -->|3. Route Request| D[🧠 Backend API (Node.js)]
    
    D -->|4. Speech-to-Text| E[🤖 Whisper ASR Module]
    
    E -->|5. Transcription| F[🧮 AI Scoring Engine]
    
    F -->|6. Score & Feedback (JSON)| D
    
    D -->|7. Response| B
    
    B -->|8. Display Results (UI)| A

🌀 Data Flow Explained
LIVE MIC MODE

User speech
→ Browser SpeechRecognition
→ Intermediate text
→ Local scoring engine
→ Result displayed instantly

UPLOAD MODE

Audio/Video
→ Backend
→ Whisper ASR
→ Segmentation
→ AI scoring
→ JSON response

💻 Technology Stack
Component	Technology	Role
Backend	Node.js (Express)	API + ASR processing
Speech Processing	Whisper ASR	High accuracy transcription
Deployment	HuggingFace Spaces	Docker-based global hosting
Mobile	Android (Kotlin) + JNI	Secure WebView container
File Handling	Multer	Upload management
Environment	dotenv	Secure variable storage
⚙️ 1. BACKEND SETUP (mentorai-backend)

The backend is responsible for:

Whisper ASR

File uploads

Segmentation

Scoring

Feedback generation

🛠 Step 1 — Clone Backend
git clone https://github.com/ProbalBoruah32/mentorai-backend.git
cd mentorai-backend

📦 Step 2 — Install Dependencies
npm install

🔐 Step 3 — Create .env
PORT=5000
HF_TOKEN=your_huggingface_token
HF_MODEL=openai/whisper-small


Token → https://huggingface.co/settings/tokens

▶️ Step 4 — Start Backend
node server.js


Expected:

Backend running on port 5000

☁️ 2. DEPLOY BACKEND ON HUGGING FACE
☁️ Step 1 — Create a HuggingFace Space

SDK: Docker

Name: mentorai-backend

Visibility: Public

🐳 Step 2 — Add Dockerfile
FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 7860
CMD ["node", "server.js"]


Modify backend:

const PORT = process.env.PORT || 7860;

🔁 Step 3 — Push to HuggingFace
git init
git remote add origin https://huggingface.co/spaces/YourUser/mentorai-backend
git add .
git commit -m "Deploy MentorAI Backend"
git push origin main


Your API becomes public at:

https://yourname-mentorai-backend.hf.space

🌐 3. WEB APPLICATION SETUP (mentoraiapplicationwork)
⬇ Step 1 — Clone
git clone https://github.com/ProbalBoruah32/mentoraiapplicationwork.git
cd mentoraiapplicationwork

🔗 Step 2 — Connect to Backend
const API_BASE_URL = "https://yourname-mentorai-backend.hf.space";

💻 Step 3 — Optional Local Preview
npx serve .


URL:

http://localhost:3000

📱 4. ANDROID APPLICATION — FULL GUIDE

MentorAI includes a secure Kotlin-based Android app with WebView.

🔒 JNI URL Protection

Backend URL stored in mentorai.cpp:

private external fun getWebUrl(): String


This prevents reverse engineering.

🌐 WebView Loads App
WebView(context).apply {
    settings.javaScriptEnabled = true
    loadUrl(getWebUrl())
}

📦 Build APK

Android Studio →

Build → Build APK(s)


Output:

app/build/outputs/apk/debug/app-debug.apk

📲 Install APK
adb install app-debug.apk

🎬 Demonstration Videos & Screenshot Slots
🎥 Introduction Video

👉 https://youtube.com/shorts/9BJNRDeTk2s?feature=share

📹 Video Slot 2 — Backend Running & API Testing
[ Insert Video Thumbnail Here ]

📹 Video Slot 3 — HuggingFace Deployment Demo
[ Insert Video Thumbnail Here ]

📹 Video Slot 4 — Android App Demonstration
[ Insert Video Thumbnail Here ]

📸 Screenshot Slots (Add Images Later)
🖼️ Architecture Diagram
[ Insert Architecture Image Here ]

🖼️ Web Interface Screenshots
[ Insert Screenshot #1 ]
[ Insert Screenshot #2 ]
[ Insert Screenshot #3 ]

🖼️ Android App Screenshots
[ Insert Android Image #1 ]
[ Insert Android Image #2 ]
[ Insert Android Image #3 ]

🤝 Credits

Developed by:
👉 Probal Boruah
MentorAI — 2025

📄 Technical Documentation (PDF Slot)
[ Insert Documentation PDF Link Here ]

