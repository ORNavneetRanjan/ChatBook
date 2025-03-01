

## Setup Instructions

### Prerequisites

Before setting up the project, make sure you have the following installed:

- **Node.js (>= 16.x)** [Download Here](https://nodejs.org/)
- **npm or yarn** (npm comes with Node.js)
- **Vite** (for fast development) [Vite Documentation](https://vitejs.dev/)

### Clone the Repository

```sh
git clone https://github.com/ORNavneetRanjan/ChatBook.git
cd chatbook
```

### Install Dependencies

Run the following command to install the required packages:

```sh
npm install
```

or

```sh
yarn install
```

### Set Up Environment Variables

Create a `.env` file in the root directory and add your API key:

```env
VITE_API_KEY=your_gemini_api_key
```

Replace `your_gemini_api_key` with your actual Google Gemini API key.

---

## Architecture Overview

This chat application is built using React (Vite) for the frontend and integrates Google Gemini API for AI-powered responses. It is designed to be lightweight, responsive, and user-friendly, with features like chat history management and a "New Conversation" reset option.

### Architecture Breakdown

#### 1️⃣ Frontend (React + Vite)

The frontend handles:
- ✅ User Interface (Chat messages, input fields, buttons, etc.)
- ✅ State Management (useState, useEffect, useRef)
- ✅ API Calls (Sending user input to the Gemini API)
- ✅ Local Storage Management (Saving and loading chat history)

**Key Components:**

| Component      | Purpose                                       |
|----------------|-----------------------------------------------|
| Home.jsx       | Main chat UI (handles user input, displays messages) |
| main.js        | Handles API integration with Google Gemini    |
| App.jsx        | Manages routing and app structure             |
| localStorage.js| Utility functions to save/load chat history   |

#### 2️⃣ Backend (Google Gemini API Integration)

There is no separate backend—the app directly communicates with Google Gemini API to generate AI responses.

**API Request Flow:**

1. User types a message and sends it.
2. The app calls `sendMessageToGemini()` (in main.js).
3. The function sends the message to Gemini API.
4. Gemini responds with text, which is displayed in the chat.

#### 3️⃣ Local Storage (Chat History Management)

The chat history is stored locally in `localStorage`, allowing users to persist conversations even after refreshing the page.

**Functions Used:**

| Function          | Purpose                            |
|-------------------|------------------------------------|
| `loadChatHistory()`| Loads previous messages from `localStorage` |
| `saveChatHistory()`| Saves new messages to `localStorage` |
| `clearChatHistory()`| Deletes all messages when starting a new conversation |

---

### App Flow Diagram

```plaintext
[ User Input ]  
     ↓  
[ sendMessageToGemini() ]  
     ↓  
[ Call Google Gemini API ]  
     ↓  
[ Receive Response ]  
     ↓  
[ Update Chat UI & Save to Local Storage ]  
```

---

### Tech Stack

| Technology          | Purpose                                    |
|---------------------|--------------------------------------------|
| React (Vite)        | Frontend framework for fast UI rendering  |
| Google Gemini API   | AI-powered chat responses                 |
| LocalStorage        | Storing conversation history              |
| Tailwind CSS        | Styling for a modern and responsive UI    |


User Guide - AI Chat Application
Welcome to the AI Chat Application! Follow the steps below to get started:

🔗 Access the App
ChatDSA

🚀 Getting Started
1️⃣ Open the Application
Hosted URL: Visit ChatDSA

Local Setup: Run npm run dev and access via http://localhost:5173/

💬 Using the Chat
2️⃣ Sending a Message
Type your message and press Send (or hit Enter).

📜 Managing Chat History
3️⃣ Viewing Past Conversations
Previous messages are saved automatically in your browser's local storage.

4️⃣ Starting a New Conversation
Click the "New Conversation" icon (📄) in the top navigation bar.

📱 Device Compatibility
Works on mobile, tablet, and desktop devices.

⚠️ Troubleshooting
Ensure a stable internet connection.

Refresh the page if the chat isn’t responding.

Start a new conversation if messages aren’t sending.
