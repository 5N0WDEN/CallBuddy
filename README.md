# CallBuddy – AI Voice Assistant Infrastructure 📞🤖

CallBuddy is an AI-powered voice assistant platform designed to handle real-time phone calls, process speech, understand user intent using NLP, and generate intelligent responses. The system integrates telephony services, backend servers, AI processing services, databases, and caching to create a scalable and modular voice automation infrastructure.

This project is currently under active development.

---

# 🚧 Project Status

**Current Phase:** Core Infrastructure and AI Processing Integration (In Progress)

This project is not production-ready yet. The backend foundation, architecture, and core communication flow have been designed and partially implemented. Active development is ongoing.

![WhatsApp Image 2026-02-17 at 14 21 14](https://github.com/user-attachments/assets/37aabc76-e725-4131-b789-ec0f3e58e578)

---

# 🔄 Currently Working On

The following components are actively being developed:

## AI Processing APIs (Django)
- Audio processing endpoints
- Transcript processing
- Intent extraction using OpenAI API
- AI response generation

## Backend and AI Service Integration
- Node.js to Django communication pipeline
- Sending transcripts and receiving AI responses
- Handling response playback flow

## Call Flow Implementation
- Complete real-time call handling logic
- Response generation and playback pipeline

---

# ⏳ Planned Features

## AI and Audio Processing
- Audio feature extraction:
  - Frequency
  - Amplitude
  - Phase
- Audio fingerprint generation
- Intent recognition and classification
- Context-aware intelligent responses

## PostgreSQL Integration
- Store AI context data
- Store processed audio patterns
- Client-specific audio and response storage

## Dashboard (Planned)
- Call logs visualization
- Transcripts viewer
- Assistant configuration
- Analytics

## Mobile App Integration (Planned)
- View call logs
- Configure assistant settings
- Monitor assistant performance

---

# 📡 Planned APIs

## Node.js Backend APIs

### Call APIs
```
POST /api/call/incoming
Handle incoming calls from Twilio
```

```
POST /api/call/control
Control call flow and playback
```

```
GET /api/call/history
Fetch call history
```

```
GET /api/call/:id
Fetch specific call details
```

---

### User APIs
```
POST /api/user/register
Register new user
```

```
GET /api/user/profile
Fetch user profile
```

---

### Assistant APIs
```
POST /api/assistant/config
Update assistant configuration
```

---

## Django AI Processing APIs

### Audio Processing API
```
POST /ai/process-audio
Extract audio features
```

### Intent Analysis API
```
POST /ai/analyze-intent
Send transcript to OpenAI and receive intent
```

### Audio Match API
```
POST /ai/match-audio
Match audio fingerprint from Redis cache
```

### Response Generation API
```
POST /ai/generate-response
Generate AI response
```

---

# 🛠️ Tech Stack

## Backend
- Node.js
- Express.js
- Django
- Python

## AI and NLP
- OpenAI API
- Natural Language Processing

## Databases
- MongoDB (Call logs, transcripts, users)
- PostgreSQL (AI context, audio patterns)

## Cache
- Redis (Audio fingerprint caching)

## Telephony
- Twilio Voice API

## DevOps (Planned)
- Docker
- Docker Compose

---

# 🐳 Dockerization Plan

This project will be fully containerized using Docker to ensure scalability, portability, and consistent deployment.

Planned containers:

- Node.js Backend Container
- Django AI Service Container
- MongoDB Container
- PostgreSQL Container
- Redis Container

Docker Compose will manage:

- Service orchestration
- Internal networking
- Environment variables
- Volume persistence

---

# 🧠 System Workflow Overview

1. Incoming call received via Twilio
2. Twilio forwards request to Node.js backend
3. Backend sends audio/transcript to Django AI service
4. Django processes audio and sends transcript to OpenAI
5. OpenAI returns intent and response
6. Django returns processed response to backend
7. Backend sends response to caller
8. Call logs and metadata stored in MongoDB
9. Redis used for caching audio fingerprints

---

# 🎯 Current Development Focus

Current priorities include:

- Completing Django AI processing APIs
- Integrating OpenAI intent analysis
- Implementing Redis caching layer
- Completing backend and AI communication
- Preparing Docker-based deployment

---

# 🔮 Future Improvements

- Real-time audio streaming support
- Multi-language assistant support
- Voice cloning integration
- Dashboard analytics
- Cloud deployment (AWS / GCP / Azure)
- Production-ready scalability improvements

---

# ⚠️ Project Note

This project is actively under development. The backend foundation, architecture, and initial integrations have been completed. AI processing, Redis caching, and full call handling flow are currently being implemented.

This repository reflects ongoing development progress.
