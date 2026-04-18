# 🎙️ AI Audio Transcriber

### Spring Boot + Spring AI + React.js

A full-stack web application that converts audio files into text using AI-powered transcription. Built using **Spring Boot (backend)**, **Spring AI (LLM integration)**, and **React.js (frontend)**.

---

## 🚀 Features

* 🎧 Upload audio files for transcription
* 🤖 AI-powered speech-to-text using Spring AI
* ⚡ REST API built with Spring Boot
* 🌐 Interactive frontend using React.js
* 🔄 Seamless frontend-backend communication
* 🎨 Basic responsive UI with CSS

---

## 🛠️ Tech Stack

### Backend

* Java
* Spring Boot
* Spring AI
* REST APIs

### Frontend

* React.js
* Axios

### Tools & Others

* Maven
* JSON

---

## 🧩 Project Structure

```
backend/
 ├── controller/
 ├── service/
 ├── config/
 └── application.properties

frontend/
 ├── components/
 ├── services/
 └── App.js
```

---

## ⚙️ Setup & Installation

### 1. Clone the Repository

```
git clone https://github.com/your-username/audio-transcriber.git
cd audio-transcriber
```

---

### 2. Backend Setup (Spring Boot)

* Open the backend folder in your IDE
* Configure your API key in `application.properties`

```
spring.ai.openai.api-key=YOUR_API_KEY
```

* Run the application

---

### 3. Frontend Setup (React)

```
cd frontend
npm install
npm start
```

---

## 🔄 How It Works

1. User uploads an audio file from the frontend
2. React sends the file to the Spring Boot backend via REST API
3. Spring AI processes the audio using an AI model
4. Transcribed text is returned to the frontend
5. UI displays the transcript to the user

---

## 📸 Demo Flow

* Upload Audio → Process → View Transcript

---

## 📌 Use Cases

* 🎓 Lecture transcription
* 📝 Voice notes conversion
* 🎙️ Podcast transcription
* 📚 Study material generation

---

## 🚧 Future Improvements

* Real-time transcription
* Multi-language support
* Transcript download (PDF/Doc)
* User authentication
* Database integration

---

## 👨‍💻 Author

**Vaibhav Gupta**

---

## ⭐ Acknowledgment

This project was built as part of learning **Spring AI and full-stack development**, focusing on integrating AI capabilities into real-world applications.
