# Prescribe AI

Doctors spend 16 hours a week on burdensome paperwork – time that could be better spent at the patient’s side delivering quality care. Additionally, almost $88 billion are spent on incorrect insurance billing every year. Prescribe AI was born out of the need to streamline medical coding and reduce these costly inefficiencies.

Prescribe AI is an intelligent assistant that leverages live speech recognition and AI to identify CPT (Current Procedural Terminology) codes directly from spoken language. In busy medical settings where documentation is time-consuming and prone to errors, Prescribe AI provides an accessible, efficient, and accurate way to generate CPT codes in real-time.

---

## Features

- **Live Speech Recognition:** Capture spoken words using the browser’s or mobile device’s built-in speech recognition capabilities.
- **Real-Time CPT Code Extraction:** Process the transcribed text with AI to extract and display relevant CPT codes quickly.
- **Patient Selection & Billing:** Select a patient directly from the front-end interface to associate the generated CPT codes with their account. Once recording stops, a bill is generated automatically.
- **Cross-Platform Support:** Includes a web interface (built with React and Flask) and a mobile version (built with Expo and React Native) for seamless integration in different clinical settings.
- **AI-Powered Accuracy:** Integrates with external AI services to provide accurate code extraction and cost estimation based on Medicare fee schedules.

---

## Architecture

- **Backend:** A Flask server that handles HTTP routes and WebSocket connections. It processes incoming transcripts, utilizes AI (via third-party services) to extract CPT codes, and manages patient selection and billing.
- **Frontend (Web):** A React-based single-page application that supports voice recording, displays real-time transcripts, and shows extracted CPT codes using interactive UI components.

- **Mobile App will be developed after web:** An Expo/React Native version designed for on-the-go usage, providing similar functionalities as the web interface.
- **Integration with External APIs:** Uses environment-configured API keys (e.g., `GROQ_API_KEY`) to interact with AI services for chat completions and cost estimations.

---

## Prerequisites

- **Backend:**
  
- **Python 3.8+**

---

## Usage(After development)

1. **Select a Patient:**  
   Use the intuitive dropdown to select a patient by their first and last name. This will set the context for the subsequent documentation and billing operations.

2. **Start Recording:**  
   Tap the microphone button to start live speech recognition. The interface will display the real-time transcript.

3. **Extract CPT Codes:**  
   As you speak, the application automatically sends the transcript to the AI-powered backend, which identifies and extracts relevant CPT codes.

4. **Stop Recording & Generate Bill:**  
   When you are finished, tap the “Stop” button. This finalizes the transcription, creates an invoice based on the extracted CPT codes, and resets the session.

5. **Review & Copy Codes:**  
   The extracted CPT codes are displayed on both the web and mobile interfaces. Easily copy any code for documentation or billing purposes with a single tap.

---

## Technologies

- **Backend:** Python, Flask, Flask-CORS, Flask-Sock, Requests
- **Frontend:** React, TypeScript(or)Javascript, Tailwind CSS
- **Mobile:** Expo, React Native, React Navigation
- **Speech Recognition:** Web Speech API (for browsers) and react-native-voice (for mobile)
- **AI Integration:** External AI services for chat completions and cost estimation