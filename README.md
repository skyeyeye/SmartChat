# ✨ Full Stack Realtime Chat App ✨ [Website Link](https://smart-chat-jet.vercel.app/)
A production-ready **MERN**-based chat application featuring **real-time messaging**, secure authentication, and online user tracking. Built with modern technologies for performance, scalability, and ease of deployment.

---
## 🚀 Highlights

- 🌟 **Tech Stack:** MongoDB, Express.js, React (Vite), Node.js, Socket.io, TailwindCSS, DaisyUI  
- 🎃 **Authentication & Authorization:** Secure JWT-based system with cookies  
- 👾 **Real-Time Messaging:** Powered by Socket.io for instant communication  
- 🚀 **Online User Status:** Live presence tracking  
- 👌 **State Management:** Global state handled by Zustand  
- 🐞 **Error Handling:** Comprehensive client & server error management  
- ⭐ **Deployment Ready:** Configured for Render (backend) and Vercel (frontend)  
- ⏳ **And much more!**

---

## 🖼 Preview
**Screenshots coming soon** 
![Chat Interface](https://github.com/user-attachments/assets/de413fb0-5bc6-4821-bb19-50232f1d4ef8)
![Image](https://github.com/user-attachments/assets/249ff6b6-a5e3-441a-8eb4-584301594da3)
![Image](https://github.com/user-attachments/assets/1c5b816f-9841-4692-86d3-ec7eefaf5b16)
![Image](https://github.com/user-attachments/assets/c3c266b3-8c11-4e54-912b-9e4b8d7adbd8)
![Image](https://github.com/user-attachments/assets/3f79a8ab-0df9-47a7-9dc1-3e588b23b758)
---
## 🛠 Tech Stack

**Frontend**
- React (Vite)
- Zustand
- TailwindCSS + DaisyUI

**Backend**
- Node.js
- Express.js
- MongoDB (Mongoose)
- Socket.io

---
## ⚡ Features

- ✅ Real-time one-to-one chat  
- ✅ JWT authentication with cookies  
- ✅ Online/offline user indicators  
- ✅ Responsive & mobile-friendly UI  
- ✅ Secure API calls (CORS + HTTPS)  
- ✅ Persistent sessions  
---
# 📡 API Endpoints

## Auth Routes
- **POST** `/api/auth/signup` → Register a new user.
- **POST** `/api/auth/login` → Login and get auth token.
- **POST** `/api/auth/logout` → Logout current user.
- **PUT** `/api/auth/update-profile` → Update user profile (requires JWT).
- **GET** `/api/auth/check` → Verify authentication (requires JWT).

## Message Routes
- **GET** `/api/messages/users` → Get all users for sidebar (requires JWT).
- **GET** `/api/messages/:id` → Fetch chat history with a user (requires JWT).
- **POST** `/api/messages/send/:id` → Send a message to a user (requires JWT).

> **Auth:** Most routes require JWT stored in cookies. Ensure `withCredentials: true` in frontend requests.
---
## ⚡ Socket.io Events
**Server → Client**
| Event Name       | Payload         | Description                       |
| ---------------- | --------------- | --------------------------------- |
| `getOnlineUsers` | `[userId, ...]` | Sends an array of online user IDs |

**Client → Server**

| Event Name    | Payload           | Description                 |
| ------------- | ----------------- | --------------------------- |
| `sendMessage` | `{ to, message }` | Sends a message to a user   |
| `disconnect`  | none              | Fires when user disconnects |
---
## 🔧 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/skyeyeye/SmartChat.git
cd SmartChat
```

### 2. Backend Setup

```bash
cd backend
npm install
``` 
Create a .env file inside the backend/ directory:
```bash
PORT=5001
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
FRONTEND_URL=https://your-frontend.vercel.app
```
Run the backend:
```bash
npm run dev
```
### 3. Frontend Setup
   
```bash
cd ../frontend
npm install
```
Create a .env file inside the frontend/ directory:
```bash
VITE_BACKEND_URL=https://your-backend.onrender.com
```
Run the frontend:
```bash
npm run dev
```
### 4. Open in Browser
  
Visit:
```bash
http://localhost:5173
```
(Default Vite dev server port)
---
### 📦 Deployment
- **Frontend: Vercel**

- **Backend: Render**

- **Database: MongoDB Atlas**

🤝 Contributing
---
- Pull requests are welcome.
- For major changes, please open an issue first.
  
💖 Made with ❤️ by Ayush Saha
  ---
