# Lingua-Forge

**Lingua-Forge** is a language learning web app built with a microservice architecture. The goal is to help learners practice vocabulary, grammar, and basic conversation using AI tools like GPT and Azure Speech. It’s still a work-in-progress, mainly for demo and learning purposes.

---

## 🔍 Overview

This project is structured around multiple backend services, each responsible for a single domain (auth, user progress, vocabulary, grammar, AI). All services are containerized using Docker and can be deployed on a single VPS.

Frontend will be added later as a separate React app (also containerized).

---

## 🧱 Microservice Architecture

Lingua-Forge consists of several main services, each responsible for a specific function:

- **API Gateway**  
  Coordinates and forwards requests between services (Nginx or YARP).

- **Auth Service**  
  Handles registration, login, and JWT authentication.  
  Stores data in PostgreSQL (`auth_db`).

- **User Service**  
  Manages user profiles and learning progress.  
  Stores data in PostgreSQL.

- **Vocab Service**  
  Manages vocabulary, flashcards, and quizzes.  
  Stores data in PostgreSQL (`vocab_db`).

- **Grammar Service**  
  Manages grammar theory and mini tests.  
  Stores data in PostgreSQL (`grammar_db`).

- **AI Service**  
  Integrates GPT and Azure Speech for feedback and speech recognition.  
  Stores data in MongoDB.

- **Frontend (React)**  
  React application (planned), hosted via Nginx.

All services are containerized with Docker and can be deployed on a single VPS.

---

### 📌 Description of Each Service

| Service           | Purpose                                              | DB         | Port |
|-------------------|------------------------------------------------------|------------|------|
| `auth-service`     | Login, register, issue/refresh JWT tokens           | PostgreSQL | 5001 |
| `user-service`     | Profile, learning progress tracking                 | PostgreSQL | 5002 |
| `vocab-service`    | Topic-based vocabulary, flashcards, basic quiz      | PostgreSQL | 5003 |
| `grammar-service`  | Grammar theory, exercises                           | PostgreSQL | 5004 |
| `ai-service`       | GPT feedback, grammar correction, speech analysis   | MongoDB    | 5005 |
| `gateway`          | Routes all traffic to correct service               | Nginx/YARP | 80/443 |
| `frontend`         | React app (coming soon)                             | N/A        | 3000 (planned) |

---

## 🛠️ Tech Stack

- **Backend**: ASP.NET Core 8 + Dapper
- **Frontend**: ReactJS (planned)
- **Database**:
  - PostgreSQL for structured data (auth, vocab, grammar, user)
  - MongoDB for AI service (storing GPT responses, speech analysis logs)
- **AI Services**: OpenAI GPT, Azure Speech-to-Text / Text-to-Speech
- **Containerization**: Docker, Docker Compose
- **Gateway**: Nginx (or YARP if using .NET reverse proxy)

---

## 🚀 Quick Start

### 1. Clone the repo

```bash
git clone https://github.com/yourname/lingua-forge.git
cd lingua-forge
```

