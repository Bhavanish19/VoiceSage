# 🎙️ VoiceSage: AI-Powered Audio Generation Platform

Welcome to **VoiceSage**, a full-stack clone of ElevenLabs that gives users the power to generate speech, convert voices, and synthesize audio effects—all **self-hosted** using state-of-the-art open-source AI models. Unlike typical tutorials that rely on external APIs, VoiceSage puts you in control by running **locally fine-tuned models** with Docker, FastAPI, and a modern web UI.


---

## 🚀 Key Features

### 🔊 AI Capabilities

* **Text-to-Speech (TTS)** with `StyleTTS2`
* **Voice Conversion** with `Seed-VC`
* **Audio/SFX Generation** with `Make-An-Audio`
* **Voice Fine-Tuning** support for custom dataset training

### ⚙️ Backend

* **FastAPI** Python backend exposing inference endpoints
* **PyTorch**-based model handling
* **Dockerized** AI service deployment for consistent environments
* **Inngest Queue** to throttle requests and prevent server overload
* **S3 Storage** for audio file storage & retrieval

### 🖥️ Frontend (T3 Stack)

* **Next.js + React** powered UI
* **Tailwind CSS** for modern styling
* **Auth.js** for secure authentication & protected routes
* **Voice Picker** and **Audio History** views
* **User Credit System** to manage compute quotas

---

## 🧠 Architecture Overview

* Each AI model runs in its own Docker container
* FastAPI routes handle inference and queueing
* Frontend interacts via REST API to send text and retrieve audio
* Inngest queue ensures inference load balancing
* AWS S3 handles persistent audio storage

---

## 💲 Cost Breakdown & Free Setup Tips

| Service           | Cost               |
| ----------------- | ------------------ |
| Model Fine-Tuning | \~\$5–10 one-time  |
| EC2 Hosting       | \~\$1/hr (if used) |
| S3 Storage        | Free <5GB          |
| IAM/Users         | Free               |

---

## 🛠️ Tech Stack

* **Frontend**: Next.js, React, Tailwind CSS, Auth.js
* **Backend**: FastAPI, PyTorch, Inngest, Docker
* **AI Models**: StyleTTS2, Seed-VC, Make-An-Audio
* **Infra**: AWS S3, EC2 (optional), IAM, Docker Compose

---

## ✅ Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Bhavanish19/VoiceSage.git
cd VoiceSage
```

### 2️⃣ Backend Setup

* Follow instructions in `/backend` for setting up FastAPI + Docker
* Pull or place pre-trained models in the models directory

### 3️⃣ Frontend Setup

```bash
cd /frontend
npm install
```

### 4️⃣ Environment Variables

Create `.env.local` with:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_AUTH_KEY=your_auth_key
AWS_BUCKET_NAME=your_bucket_name
```

### 5️⃣ Run Locally

* Start backend with Docker Compose

```bash
docker-compose up --build
```

* Start frontend

```bash
npm run dev
```

Visit: `http://localhost:3000`

---

## 📦 Deployment

VoiceSage supports EC2 + Docker Compose deployment. Check `deploy/` folder for Terraform, AWS IAM policies, and step-by-step EC2 deployment script.

---

## 📈 Roadmap

* 🎙️ Add microphone recording input
* 🌐 International language support for TTS
* 📊 Usage analytics dashboard
* 🧠 HuggingFace Hub integration for model sharing

---

## 🙌 Contributing

PRs are welcome! Please fork the repo and submit a pull request for any new features or improvements.

---

## 👨‍💻 Developed with by Bhavanish Dhamnaskar

Website: [bhavanish.com](https://bhavanish.com)
GitHub: [@Bhavanish19](https://github.com/Bhavanish19)

---
