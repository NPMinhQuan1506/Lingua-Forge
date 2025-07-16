# Lingua-Forge – Draft Business Function Diagram (BFD)

This draft outlines the top-level functions grouped by service. Each block below corresponds to a microservice.

---

## 1. user-service

**Main Actor**: User  
**Functions**:
- Register / Login
- View profile
- Update user info
- Change password

---

## 2. learning-service

**Main Actor**: User  
**Functions**:
- Get list of vocabulary topics
- Learn flashcard by topic
- Take vocabulary quiz
- View grammar lesson
- Take grammar quiz

---

## 3. progress-tracking

**Main Actor**: System  
**Functions**:
- Log quiz results
- Log completed lessons
- Retrieve learning history
- Export learning summary

---

## 4. ai-speech-service

**Main Actor**: User  
**Functions**:
- Submit audio for speech recognition
- Receive transcribed text from Azure
- Compare user speech to expected answer

---

## 5. ai-custom-service

**Main Actor**: User  
**Functions**:
- Submit writing for grammar check
- Receive correction + explanation
- Word meaning clarification
- Suggest similar phrases

---

## 6. frontend (ReactJS)

**Main Actor**: User  
**Functions**:
- Navigate dashboard
- Access learning modules (vocab, grammar, writing)
- Display progress chart
- Trigger speech / writing AI
