# My Chat App

A real-time web chat application with a React + Vite frontend and a Node.js + Express backend providing authentication, user profiles, and socket-based messaging.

**TL;DR**: Modern full-stack chat app demonstrating real-time messaging with `socket.io`, user auth, and a responsive React UI.

**Features**
- **Real-time messaging**: Socket-based chat using `socket.io` (`socket.io` on server and `socket.io-client` on client).
- **User authentication**: Signup/login flows with hashed passwords (`bcrypt`) and JWTs (`jsonwebtoken`).
- **Persistent storage**: MongoDB models for users and messages via `mongoose`.
- **Responsive React UI**: Built with React + Vite and styled components, including message input, contact list, and avatar setup.
- **Utilities**: API routes and helpers for client-server communication, file-based assets, and environment configuration.

**Why this project**
- Demonstrates building a complete real-time application combining frontend and backend concerns.
- Shows usage of modern React tooling (Vite) and real-time networking with `socket.io`.
- Useful reference for authentication, database modeling, and connecting a React client to a Node/Express API.

**Tech Stack**
- **Frontend**: React (Vite), `axios`, `socket.io-client`, `react-router`, `styled-components`, `react-toastify`.
- **Backend**: Node.js, Express, `socket.io`, `mongoose`, `jsonwebtoken`, `bcrypt`, `cors`, `dotenv`.
- **Dev tools**: `nodemon` for server dev; Vite dev server for client.

**Project Structure** (high level)
- **client/**: React app using Vite. Key files:
  - `src/` — React components, pages, assets, and `utils/APIRoutes.jsx`.
  - `package.json` — frontend dependencies and scripts.
- **server/**: Express backend. Key files:
  - `index.js` — server entry point and socket initialization.
  - `routes/` — API route definitions for auth and messages.
  - `controllers/` — request handlers (auth, user, messages).
  - `models/` — Mongoose models for `user` and `message`.

**Table of Contents**
- Installation
- Environment
- Run (Development)
- Production Build
- Usage
- File map
- Future improvements
- Contributing

**Installation**
- Prerequisites:
  - Node.js (>=16)
  - npm or yarn
  - MongoDB instance (local or cloud e.g., MongoDB Atlas)

1. Clone the repository:

```bash
git clone <repo-url>
cd My-chat-app
```

2. Install server dependencies and configure environment:

```bash
cd server
npm install
```

Create a `.env` file in `server/` with at least:

```
PORT=5000
MONGO_URL=<your-mongodb-connection-string>
JWT_SECRET=<a-strong-secret>
FRONTEND_URL=http://localhost:5173
```

3. Install client dependencies:

```bash
cd ../client
npm install
```

**Run (Development)**
- Start server (from `server/`):

```bash
npm run dev
```

- Start client (from `client/`):

```bash
npm run dev
```

Open the client URL shown by Vite (default: `http://localhost:5173`). The client communicates with the backend and establishes socket connections for real-time messaging.

**Production Build**
- Build client:

```bash
cd client
npm run build
```

- Serve the built client with any static server (or integrate into Express static middleware). Ensure the server `FRONTEND_URL`/CORS and socket origins are configured to allow connections.

**How to Use**
- Register a new user via the Register page.
- Set an avatar via the Set Avatar page to personalize your profile.
- Add contacts or select a conversation from the contacts list to begin messaging.
- Messages are sent in real time; multiple clients will see messages instantly via sockets.

**Credentials for Local Development**
- No default credentials are provided. Create accounts using the Register flow.

**File Map (important files)**
- `server/index.js` — Entry point and socket setup.
- `server/routes/authRoutes.js` — Signup/login endpoints.
- `server/routes/messageRoutes.js` — Message history and send endpoints.
- `server/models/userModel.js` — Mongoose user schema.
- `server/models/messageModel.js` — Mongoose message schema.
- `client/src/App.jsx` — React app root and router.
- `client/src/utils/APIRoutes.jsx` — Client API endpoints and routes.

**Future Improvements**
- Add message read receipts and typing indicators.
- Add file/image attachments and storage (e.g., S3).
- Add end-to-end tests and CI pipeline.
- Optimize offline message queuing and reconnection handling.

**Contributing**
- Fork the repo, create a feature branch, and open a pull request describing your changes.
- Keep changes focused and add tests where applicable.

**Contact / Questions**
- For questions about running or extending the project, open an issue or contact the maintainer.
