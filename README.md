# Lingua-Forge

**Lingua-Forge** is a side project I’m building to explore how AI can support language learning. It’s still in early stages and mainly serves as a demo. If things go well, I might develop it further later on.

---

## 📌 What It’s About

The idea is to create a simple web app to help users (currently English learners) practice:
- Vocabulary by topic
- Basic grammar
- Listening and speaking (early phase)
- AI-assisted features like feedback and pronunciation

Tech stack is pretty standard: .NET Core for the backend, React for the frontend, PostgreSQL for the database. Everything runs in Docker containers for simplicity.

---

## 🔧 Tech Stack

- .NET 8 + Dapper (Web API)
- ReactJS (Frontend)
- PostgreSQL (Database)
- Docker + Docker Compose
- GPT API (OpenAI or Azure)
- Azure Speech Services (for speech-to-text and pronunciation)

---

## 🚀 How to Run It

This assumes you’re a developer and already have Docker installed.

### 1. Clone the repo

```bash
git clone https://github.com/yourname/lingua-forge.git
cd lingua-forge
