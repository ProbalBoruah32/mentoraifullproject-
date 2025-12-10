![Status](https://img.shields.io/badge/Project%20Status-Active-brightgreen)
![Build](https://img.shields.io/badge/Build-Passing-success)
![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![Platform-Android](https://img.shields.io/badge/Platform-Android%20%7C%20Web-blueviolet)

🌟 MentorAI: 

AI-Powered Communication Assessment Ecosystem 🗣️
A Complete End-to-End Platform for Real-Time Speech Analysis, Intelligent Scoring, and Skill Improvement
🛡️ Project Status & Technology Stack
Category	Status	Tech Used
Project Status	✔️ Active	—
Backend	✔️ Node.js, HuggingFace	Whisper ASR
AI / ML	✔️ Integrated	Whisper + Scoring Engine
Frontend / Mobile	✔️ Web App + Android	Kotlin + JNI


<img width="1024" height="1024" alt="mentor_ai_logo" src="https://github.com/user-attachments/assets/6560ad35-0a5c-4204-9305-38fa38af2cdc" />
click here to see our demo https://youtube.com/shorts/9BJNRDeTk2s?feature=share



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

![Whisper ASR](https://img.shields.io/badge/AI-Whisper%20ASR-orange)
![Node.js](https://img.shields.io/badge/Backend-Node.js-green)
![HuggingFace](https://img.shields.io/badge/Deploy-HuggingFace-yellow)
![Android](https://img.shields.io/badge/Mobile-Kotlin-green)


It includes:

🎤 Real-time Microphone Transcription
🤖 Whisper ASR (Speech-to-Text)
🧮 AI-based Scoring Engine (0–10 scale)
📱 Android App with WebView + JNI URL Protection
🌐 Fully Hosted Backend on HuggingFace
training dashboard https://huggingface.co/prob12/whisper_trainin4_language/tensorboard

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
<img width="1252" height="757" alt="image" src="https://github.com/user-attachments/assets/ca7ac5da-c237-43a6-a788-d0e60977231c" />
https://colab.research.google.com/drive/1tYlVIqwibpUkZkI7Pob5RxUxsxRo9d0-?usp=sharing      initial train 



MentorAI’s architecture is modular, flexible, and interconnected.

📁 Project Structure

MentorAI /

 ├── mentorai-backend/           # Node.js backend + Whisper ASR + AI scoring engine
 
 ├── mentoraiapplicationwork/    # Frontend scoring interface & audio/video workflow
 
 └── android-app/                # Secure Android app using WebView + JNI

🏗️ Architecture Diagram 


<img width="1536" height="1024" alt="40f591b5-bf63-4bc2-b369-bff421166937" src="https://github.com/user-attachments/assets/71c46094-a03a-4dc8-bc81-0a3539df8f2c" />
![API Ready](https://img.shields.io/badge/API-REST%20Ready-blue)
![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED)
![Security](https://img.shields.io/badge/Security-URL%20Protected-red)


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
<img width="1433" height="827" alt="image" src="https://github.com/user-attachments/assets/9c6546f7-4f07-4379-afcb-4c68233b1171" />
 click here to watch how run it https://youtu.be/T6JRS9pWQiI

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
📱 4. ANDROID APPLICATION — FULL GUIDE (WebView Removed)

MentorAI includes a secure Kotlin-based Android application that integrates with the AI backend and provides an intuitive user flow with login, profile, and secure native logic through JNI.

🔽 Step 1 — Clone the Android App Repository
git clone https://github.com/ProbalBoruah32/mentoraiapplicationwork.git
cd mentoraiapplicationwork

🧰 Step 2 — Open the Project in Android Studio

1️⃣ Open Android Studio
2️⃣ Click Open Project
3️⃣ Select the folder:

mentoraiapplicationwork/


4️⃣ Allow Gradle to sync completely

Your Android environment is ready.

🔐 JNI Security Layer (Backend URL Protection)

To prevent exposure of sensitive endpoints, the backend URL is stored in native C++ code inside mentorai.cpp.

Kotlin retrieves it through:

private external fun getWebUrl(): String


This method provides:

✔ Increased security
✔ Obfuscated URL access
✔ Protection against static code analysis

▶ Step 3 — Run the App on an Emulator or Physical Device

1️⃣ Connect a device (enable USB Debugging)
or
2️⃣ Start an Android Emulator

Then click:

Run ▶


The app will launch with:

✔ Login screen
✔ App logo transition
✔ Main interface
✔ Profile icon and user state

📦 Step 4 — Build the APK

In Android Studio:

Build → Build APK(s)


APK output:

app/build/outputs/apk/debug/app-debug.apk

📲 Step 5 — Install APK on a Device
Option A — Manual Install

Transfer the APK to your phone → tap → Install.

Option B — ADB Install
adb install app-debug.apk

⭐ (Optional) Step 6 — Generate Signed APK for Release

If you want a production-ready APK:

Build → Generate Signed Bundle / APK
![Status](https://img.shields.io/badge/Project%20Status-Active-brightgreen)
![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Web-blueviolet)
![Whisper ASR](https://img.shields.io/badge/AI-Whisper%20ASR-orange)
![HuggingFace](https://img.shields.io/badge/Deploy-HuggingFace-yellow)
![API Level](https://img.shields.io/badge/Android%20API-24--35-blue)


Follow steps to create keystore → generate release APK.

![WhatsApp Image 2025-12-10 at 04 58 40_47bc6998](https://github.com/user-attachments/assets/f205ab21-9a7b-422e-9de4-1de3ac1a6a4d)


📱 Android Application (APK Download + Installation Guide)

The MentorAI Android application is provided as a compiled release build to allow evaluators and users to experience the platform directly on a mobile device.

This APK has been tested and confirmed to work on:

Android API Level: 35 (Android 14)

Minimum Supported API Level: 24+

Architecture: ARM64 / Universal Build

Package: app-release.apk

📥 Download the APK

You can download the official build here:

👉 Download app-release.apk
🔗 https://drive.google.com/file/d/1ZNBD_HVJ9_yvcL83zxKhrPisYfw5jBVV/view?usp=sharing

File Details

Property	Value
File Name	app-release.apk
Source Folder	C:\Users\pb168\AndroidStudioProjects\mentorai\app\release\app-release.apk
Build Type	Release
Platform	Android
Status	Ready to Install
📲 How to Install on Your Android Device

Follow these steps to install MentorAI on any modern Android device:

1️⃣ Download the APK

Download app-release.apk from the link above.

2️⃣ Open the File

Navigate to your Downloads folder and tap the file.

3️⃣ Allow Installation Permissions

If prompted, enable:

Settings → Security → Install unknown apps

4️⃣ Install the Application

Tap Install and wait for installation to complete.

5️⃣ Launch MentorAI

Find it in:

App Drawer → MentorAI

⚠️ Important Notice About Backend Functionality

Some features in the APK depend on a backend server for:

Whisper ASR (speech-to-text)

AI scoring

File evaluation (audio/video)

Translation

Segment analysis

📌 On a mobile device, the APK cannot access your personal localhost backend (http://localhost:5000
).

This means:

Feature	Behavior Without Online Backend
Live mic scoring	Partially works (local scoring fallback)
Upload & Score (ASR)	Disabled / Limited
Segment scoring	Disabled / Limited
Backend translation	Disabled

To achieve full functionality, the user must connect the app to a public backend URL such as:

Hugging Face Space deployment

Render / Vercel backend

Custom server

Once deployed, the backend URL can be configured in the application’s settings or internal configuration file to enable all AI features.

📝 Why APK Is Hosted on Google Drive

GitHub may block APK uploads due to:

File-size restrictions

Branch protection rules

LFS limitations

To ensure reliable access for judges and reviewers, the APK is hosted externally via Google Drive.

This ensures:

✔ 100% download success
✔ Direct installation


🤝 Credits

Developed by:
👉 Probal Boruah
MentorAI — 2025
<img width="515" height="838" alt="image" src="https://github.com/user-attachments/assets/2d498cd2-177f-4ee8-b4d2-da20cbe3ff57" />

<img width="521" height="825" alt="Screenshot 2025-12-10 081533" src="https://github.com/user-attachments/assets/d7160031-a1c1-470d-9fc5-9d524c8a6d4f" />

mentorai.docs in the repository is the document of our project 

