# Lingua-Forge – Requirements Specification (MCP Version)

## 1. Project Overview

Lingua-Forge is a personal English learning platform. The goal is to support self-paced learning with minimal setup, low cost, and optional AI enhancement.

---

## 2. Functional Requirements (for MVP/MCP)

### Learning Core

- [ ] Learn vocabulary by topic using flashcards
- [ ] Learn grammar via structured lessons
- [ ] Take quizzes (multiple-choice) after each lesson

### Listening & Speaking

- [ ] Practice listening with audio content
- [ ] Use Azure Speech-to-Text to practice speaking (say a sentence → get feedback)

### Writing + AI feedback

- [ ] Write simple paragraphs and get feedback using GPT or custom AI
- [ ] AI returns grammar corrections, clarity tips, and explanation of mistakes

### Progress Tracking

- [ ] Log lesson completions, quiz scores
- [ ] Store progress timeline in MongoDB

### User Management

- [ ] Register/Login (JWT or Firebase)
- [ ] View/update profile (email, nickname, preferred level)

---

## 3. Non-Functional Requirements

- Must be lightweight and responsive (mobile-friendly)
- Use free-tier hosting (Vercel, Railway, Render, Hugging Face)
- Backend is containerized via Docker Compose
- Separate services by domain (user, learning, AI...)
- MongoDB used for AI log and tracking
- PostgreSQL used for core learning content and user info

---

## 4. Out of Scope (For Now)

- No classroom or teacher system
- No real-time chat or social learning features
- No gamification (ranking, streak, etc.) — can be added later
