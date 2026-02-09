# 💬 Real-Time Messenger (MERN Stack)

A professional, full-stack real-time communication platform built using the MERN stack. This application leverages WebSockets for instantaneous messaging and features a modern, responsive UI designed for a seamless user experience.

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen?style=for-the-badge&logo=render)](https://kath-chat-app.onrender.com/)
[![GitHub](https://img.shields.io/badge/github-repo-black?style=for-the-badge&logo=github)](https://github.com/Kath1512/My-chat-app)
[![Tech](https://img.shields.io/badge/stack-MERN-blue?style=for-the-badge)](https://www.mongodb.com/mern-stack)

---

## 🌟 Key Features

* **Bidirectional Communication:** Low-latency messaging powered by **Socket.io**.
* **Real-time Presence:** Live "Online/Offline" status indicators for all users.
* **Secure Authentication:** Robust session management using **JSON Web Tokens (JWT)** and **Bcrypt** password hashing.
* **State Management:** Optimized client-side state handling with **Zustand**.
* **Responsive Design:** Fully adaptive UI built with **Tailwind CSS** and **DaisyUI**, featuring both Light and Dark mode support.
* **Image Support:** Integrated support for sending image-based messages.

---

## 🛠 Technical Architecture

The application is split into two main layers: a reactive frontend and a scalable backend.

### Frontend
- **React.js**: Functional components with Hooks for UI logic.
- **Tailwind CSS**: Utility-first styling for a custom, professional look.
- **Zustand**: Lightweight, centralized state management to handle chat history and user sessions.

### Backend
- **Node.js & Express**: RESTful API and WebSocket server orchestration.
- **MongoDB**: Document-based storage for users and message history.
- **Socket.io**: Manages the persistent connection between clients for real-time events.



---

## 🚀 Getting Started

### Prerequisites
- **Node.js** (v18 or higher recommended)
- **MongoDB** account (local or Atlas)

### 1. Installation
Clone the repository:
```bash
git clone [https://github.com/Kath1512/My-chat-app.git](https://github.com/Kath1512/My-chat-app.git)
cd My-chat-app
