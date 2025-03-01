Setup Instructions

Prerequisites

Before setting up the project, make sure you have the following installed:

Node.js(>= 16.x)

npm or yarn (npm comes with Node.js)

Vite (for fast development) Vite Documentation

Clone the Repository

git clone [https://github.com/your-username/your-repo-name.git](https://github.com/ORNavneetRanjan/ChatBook.git)

cd chatbook

Install Dependencies

Run the following command to install the required packages:

npm install
or
yarn install

Set Up Environment Variables

Create a .env file in the root directory and add your API key:

VITE_API_KEY=your_gemini_api_key
Replace your_gemini_api_key with your actual Google Gemini API key.


Architecture Overview
This chat application is built using React (Vite) for the frontend and integrates Google Gemini API for AI-powered responses. It is designed to be lightweight, responsive, and user-friendly, with features like chat history management and a "New Conversation" reset option.

📌 Architecture Breakdown
1️⃣ Frontend (React + Vite)
The frontend handles: ✅ User Interface (Chat messages, input fields, buttons, etc.)
✅ State Management (useState, useEffect, useRef)
✅ API Calls (Sending user input to the Gemini API)
✅ Local Storage Management (Saving and loading chat history)

📌 Key Components
Component	Purpose
Home.jsx	Main chat UI (handles user input, displays messages)
main.js	Handles API integration with Google Gemini
App.jsx	Manages routing and app structure
localStorage.js	Utility functions to save/load chat history
2️⃣ Backend (Google Gemini API Integration)
There is no separate backend—the app directly communicates with Google Gemini API to generate AI responses.

✔ API Request Flow:

User types a message and sends it.
The app calls sendMessageToGemini() (in main.js).
The function sends the message to Gemini API.
Gemini responds with text, which is displayed in the chat.
3️⃣ Local Storage (Chat History Management)
The chat history is stored locally in localStorage, allowing users to persist conversations even after refreshing the page.

✔ Functions Used:

Function	Purpose
loadChatHistory()	Loads previous messages from localStorage
saveChatHistory()	Saves new messages to localStorage
clearChatHistory()	Deletes all messages when starting a new conversation
📌 App Flow Diagram
pgsql
Copy
Edit
[ User Input ]  
     ↓  
[ sendMessageToGemini() ]  
     ↓  
[ Call Google Gemini API ]  
     ↓  
[ Receive Response ]  
     ↓  
[ Update Chat UI & Save to Local Storage ]  
📌 Tech Stack
Technology	Purpose
React (Vite)	Frontend framework for fast UI rendering
Google Gemini API	AI-powered chat responses
LocalStorage	Storing conversation history
Tailwind CSS	Styling for a modern and responsive UI
