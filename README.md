# 🤖 Shridevi Chatbot  

An AI-powered chatbot built with the **Rasa Framework**, designed to provide smart, contextual responses.  
This project was developed as a hands-on experiment in **Conversational AI** — from setting up the environment to deploying with REST APIs.  

---

## 🚀 Project Overview  
Shridevi Chatbot leverages the **Rasa open-source framework** to deliver intelligent, domain-specific conversations.  
The project demonstrates:  
- Building a chatbot from scratch  
- Customizing YAML configuration files  
- Integrating with REST APIs  
- Deploying on a scalable architecture  

---

## 🛠️ Tech Stack  

| Technology / Tool | Purpose |
|--------------------|---------|
| **Python** | Core programming language |
| **Rasa Framework** | Natural Language Understanding (NLU) + Dialogue Management |
| **YAML** | Training data, stories, domain, pipeline & configuration |
| **REST API (Default Rasa REST channel)** | External integrations for communication |
| **Virtual Environment (venv)** | Isolated environment for dependency management |
| **SQLite / JSON Store** | Storing conversation data (if needed) |
| **Postman / cURL** | API testing |

---

## ⚙️ Setup & Environment  

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/shridevi-chatbot.git
   cd shridevi-chatbot
   ```

2. **Create Virtual Environment**  
   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/Mac
   venv\Scripts\activate      # Windows
   ```

3. **Install Rasa & Dependencies**  
   ```bash
   pip install rasa
   ```

4. **Initialize Rasa Project**  
   ```bash
   rasa init
   ```

---

## 📂 Project Structure  

```
shridevi-chatbot/
│── data/
│   ├── nlu.yml          # Training data for intents
│   ├── stories.yml      # Example conversations
│── domain.yml           # Intents, entities, slots, responses
│── config.yml           # Pipeline and policies
│── endpoints.yml        # REST API / Custom connectors
│── actions.py           # Custom actions (Python)
│── credentials.yml      # API channels (REST enabled)
```

---

## 🔌 REST API Integration  

Rasa provides a default **REST API channel**.  
Enable it in `credentials.yml`:  

```yaml
rest:
```

Start the server:  
```bash
rasa run --enable-api -m models --cors "*"
```

Example request:  
```bash
curl -X POST \
  http://localhost:5005/webhooks/rest/webhook \
  -H 'Content-Type: application/json' \
  -d '{
    "sender": "user1",
    "message": "Hello Shridevi!"
}'
```

Response:  
```json
[
  {
    "recipient_id": "user1",
    "text": "Hey! I am Shridevi Chatbot. How can I help you today?"
  }
]
```

---

## ✨ Key Features  

✅ Custom NLU training with `nlu.yml`  
✅ Interactive conversation flows with `stories.yml`  
✅ Default **REST API** support for frontend integration  
✅ Environment-based setup (venv)  
✅ Extendable with **custom actions** in `actions.py`  

---

## 🎯 Future Enhancements  

- 🌍 Multilingual support (Kannada + English)  
- 💬 Deploying as a Web Chat Widget  
- ☁️ Hosting on Cloud (Heroku / AWS)  
- 📊 Analytics dashboard for conversations  

---

## 👩‍💻 Author  

Developed 
by *Heena Khanum*  

---
