# Audio to Text Transcriber

A full-stack web application that uploads an audio file, sends it to a Spring Boot backend, and returns an AI-generated transcription using OpenAI Whisper through Spring AI.

## Overview

This project consists of two parts:

- A backend API built with Java, Spring Boot, and Spring AI
- A frontend interface built with React and Vite

The app lets users upload audio files from the browser, sends them to the backend, and displays the transcribed text in the UI.

## Features

- Upload audio files from the browser
- Send audio to a REST API for transcription
- Use OpenAI Whisper for speech-to-text conversion
- Display the transcription result in the frontend
- CORS-enabled communication between frontend and backend

## Tech Stack

### Backend
- Java 21
- Spring Boot 3.3.5
- Spring AI
- OpenAI audio transcription integration
- Maven

### Frontend
- React 19
- Vite
- Axios
- CSS

## Project Structure

```text
Audio to Text Transcriber/
├── audio-transcribe/                 # Spring Boot backend
│   ├── src/main/java/com/audio/transcribe/
│   │   ├── AudioTranscribeApplication.java
│   │   ├── TranscriptionController.java
│   │   └── WebConfig.java
│   ├── src/main/resources/application.properties
│   └── pom.xml
├── Audio-transcribe-frontend/        # React frontend
│   ├── src/
│   │   ├── App.jsx
│   │   ├── AudioUploader.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
└── README.md
```

## Prerequisites

Before running the project, make sure you have:

- Java 21 or later
- Maven
- Node.js and npm
- An OpenAI API key

## Backend Setup

1. Open a terminal in the backend folder:

```bash
cd audio-transcribe
```

2. Set your OpenAI API key as an environment variable.

On PowerShell:

```powershell
$env:API_KEY="your_openai_api_key"
```

On macOS/Linux:

```bash
export API_KEY="your_openai_api_key"
```

3. Start the backend server:

```bash
./mvnw spring-boot:run
```

On Windows, you can use:

```powershell
mvnw.cmd spring-boot:run
```

The backend will run on:

```text
http://localhost:8080
```

## Frontend Setup

1. Open a second terminal in the frontend folder:

```bash
cd Audio-transcribe-frontend
```

2. Install dependencies:

```bash
npm install
```

3. Start the Vite development server:

```bash
npm run dev
```

The frontend will run on:

```text
http://localhost:5173
```

## How It Works

1. The user selects an audio file in the React UI.
2. The frontend sends the file to the backend endpoint at `/api/transcribe`.
3. The Spring Boot backend writes the uploaded file to a temporary location.
4. Spring AI sends the file to OpenAI Whisper for transcription.
5. The transcribed text is returned to the frontend and displayed on the page.

## API Endpoint

### Upload and transcribe audio

```http
POST /api/transcribe
Content-Type: multipart/form-data
```

Form field:

- `file`: audio file to transcribe

Example with curl:

```bash
curl -X POST http://localhost:8080/api/transcribe \
  -F "file=@/path/to/audio.wav"
```

## Configuration Notes

The backend is configured in [audio-transcribe/src/main/resources/application.properties](audio-transcribe/src/main/resources/application.properties) to use:

- the OpenAI API key from the `API_KEY` environment variable
- the Whisper transcription model
- the default English language setting

The frontend is configured to call the backend at `http://localhost:8080`.

## Future Improvements

Possible enhancements for this project include:

- Support for multiple languages
- Real-time or streaming transcription
- Better error handling and loading states
- Transcript download as text or file
- User authentication and saved history

## Author

Vaibhav Gupta
