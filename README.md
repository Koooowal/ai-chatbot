

# 🤖 KoowalAI ChatBot

### Full-Stack AI Chatbot Application

[![React](https://img.shields.io/badge/React-19.0.0-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-5.1.0-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-8.0-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Gemini AI](https://img.shields.io/badge/Gemini_AI-1.5_Flash-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)


[Features](#-features) •
[Tech Stack](#-tech-stack) •
[Getting Started](#-getting-started) •
[Environment Variables](#-environment-variables) •
[API Endpoints](#-api-endpoints) •
[License](#-license)


---

## ✨ Features

- 🔐 **Secure Authentication** - User authentication powered by Clerk with sign-up/sign-in flows
- 💬 **Real-time Chat** - Streaming AI responses with Google Gemini 1.5 Flash model
- 🖼️ **Image Analysis** - Upload and analyze images using multimodal AI capabilities
- 📝 **Markdown Support** - Rich text rendering for AI responses with code highlighting
- 💾 **Chat History** - Persistent conversation storage with MongoDB
- 📱 **Responsive Design** - Modern UI that works seamlessly on desktop and mobile
- ⚡ **Optimized Performance** - React Query for efficient data fetching and caching
- 🎨 **Animated Interface** - Smooth typing animations and interactive elements

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| **React 19** | UI Framework |
| **Vite** | Build Tool & Dev Server |
| **React Router 7** | Client-side Routing |
| **TanStack Query** | Server State Management |
| **Clerk React** | Authentication UI |
| **React Markdown** | AI Response Rendering |
| **ImageKit React** | Image Upload & Optimization |

### Backend
| Technology | Purpose |
|------------|---------|
| **Node.js** | Runtime Environment |
| **Express 5** | Web Framework |
| **MongoDB** | Database |
| **Mongoose** | ODM for MongoDB |
| **Clerk SDK** | Authentication Middleware |
| **ImageKit** | Image Storage & CDN |

### AI & Services
| Service | Purpose |
|---------|---------|
| **Google Gemini AI** | LLM for Chat Responses |
| **ImageKit** | Image Upload & Processing |
| **Clerk** | User Authentication |

---

## 📸 Screenshots






---

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18.x or higher
- **MongoDB** (local installation or MongoDB Atlas)
- **npm** or **yarn**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/KoowalAI_ChatBot_FullStack.git
   cd KoowalAI_ChatBot_FullStack
   ```

2. **Install Backend dependencies**
   ```bash
   cd Backend
   npm install
   ```

3. **Install Frontend dependencies**
   ```bash
   cd ../Frontend
   npm install
   ```

4. **Set up environment variables** (see [Environment Variables](#-environment-variables))

5. **Start the Backend server**
   ```bash
   cd Backend
   npm start
   # or with nodemon for development
   npx nodemon index.js
   ```

6. **Start the Frontend development server**
   ```bash
   cd Frontend
   npm run dev
   ```

7. **Open your browser** and navigate to `http://localhost:5173`

---

## 🔐 Environment Variables

### Backend (`Backend/.env`)

```env
# Server
PORT=5000
CLIENT_URL=http://localhost:5173

# MongoDB
MONGODB_URI=mongodb+srv://your-connection-string

# Clerk Authentication
CLERK_SECRET_KEY=sk_test_xxxxxxxxxxxxx
CLERK_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxx

# ImageKit
IMAGEKIT_PUBLIC_KEY=public_xxxxxxxxxxxxx
IMAGEKIT_PRIVATE_KEY=private_xxxxxxxxxxxxx
IMAGEKIT_URL_ENDPOINT=https://ik.imagekit.io/your-id
```

### Frontend (`Frontend/.env`)

```env
# API
VITE_API_ENDPOINT=http://localhost:5000

# Clerk Authentication
VITE_CLERK_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxx

# Google Gemini AI
VITE_GEMINI_KEY=AIzaSyxxxxxxxxxxxxx

# ImageKit
VITE_IK_ENDPOINT=https://ik.imagekit.io/your-id
VITE_IK_PUBLIC_KEY=public_xxxxxxxxxxxxx
```

---

## 📡 API Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `GET` | `/api/upload` | Get ImageKit auth parameters | ❌ |
| `POST` | `/api/chat` | Create a new chat | ✅ |
| `GET` | `/api/userChats` | Get all user's chats | ✅ |
| `GET` | `/api/chat/:id` | Get specific chat by ID | ✅ |
| `PUT` | `/api/chat/:id` | Add message to chat | ✅ |

---

## 📁 Project Structure

```
KoowalAI_ChatBot_FullStack/
├── 📂 Backend/
│   ├── 📂 db/
│   │   └── db.js              # MongoDB connection
│   ├── 📂 Models/
│   │   ├── chat.model.js      # Chat schema
│   │   └── userChats.model.js # User chats schema
│   ├── index.js               # Express server & routes
│   └── package.json
│
├── 📂 Frontend/
│   ├── 📂 public/             # Static assets
│   ├── 📂 src/
│   │   ├── 📂 Components/
│   │   │   ├── ChatList/      # Sidebar chat list
│   │   │   ├── NewPrompt/     # Chat input component
│   │   │   └── Upload/        # Image upload handler
│   │   ├── 📂 Layouts/
│   │   │   ├── DashboardLayout/
│   │   │   └── RootLayout/
│   │   ├── 📂 Lib/
│   │   │   └── gemini.js      # Gemini AI configuration
│   │   ├── 📂 Routes/
│   │   │   ├── ChatPage/      # Individual chat view
│   │   │   ├── DashboardPage/ # Main dashboard
│   │   │   ├── HomePage/      # Landing page
│   │   │   ├── SignInPage/    # Authentication
│   │   │   └── SignUpPage/
│   │   ├── App.jsx            # Route configuration
│   │   └── main.jsx           # App entry point
│   └── package.json
│
└── README.md
```

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

---


### 💡 Example Repository Descriptions



#### 📌 GitHub Short Description
```
🤖 Full-stack AI chatbot with Google Gemini, React 19, Node.js, Express & MongoDB. Features real-time streaming, image analysis, and Clerk authentication.
```

#### 📌 LinkedIn / Portfolio (PL)
```
🤖 KoowalAI ChatBot - Fullstack aplikacja AI Chatbot

Stworzyłem nowoczesną aplikację chatbota AI wykorzystującą Google Gemini 1.5 Flash. 
Projekt obejmuje kompletny stack: React 19, Node.js, Express.js i MongoDB.

Główne funkcjonalności:
• Streamowanie odpowiedzi AI w czasie rzeczywistym
• Analiza obrazów z wykorzystaniem multimodalnego AI
• Bezpieczna autoryzacja użytkowników (Clerk)
• Persystentna historia konwersacji
• Responsywny, nowoczesny interfejs

Tech Stack: React, Node.js, Express, MongoDB, Google Gemini AI, Clerk, ImageKit
```

#### 📌 LinkedIn / Portfolio (EN)
```
🤖 KoowalAI ChatBot - Full-Stack AI Chatbot Application

Built a modern AI chatbot application powered by Google Gemini 1.5 Flash.
Complete full-stack project featuring React 19, Node.js, Express.js, and MongoDB.

Key Features:
• Real-time AI response streaming
• Image analysis with multimodal AI capabilities
• Secure user authentication (Clerk)
• Persistent conversation history
• Responsive, modern UI design

Tech Stack: React, Node.js, Express, MongoDB, Google Gemini AI, Clerk, ImageKit
```

#### 📌 CV / Resume (Short)
```
KoowalAI ChatBot | React, Node.js, Express, MongoDB, Gemini AI
• Developed full-stack AI chatbot with real-time streaming responses
• Implemented multimodal image analysis and secure JWT authentication
• Designed RESTful API with MongoDB for persistent chat storage
```

#### 📌 CV / Resume (PL - Short)
```
KoowalAI ChatBot | React, Node.js, Express, MongoDB, Gemini AI
• Opracowałem fullstack chatbot AI ze streamowaniem odpowiedzi w czasie rzeczywistym
• Zaimplementowałem multimodalną analizę obrazów i bezpieczną autoryzację JWT
• Zaprojektowałem RESTful API z MongoDB do przechowywania historii konwersacji
```

---


Made with ❤️ by **Koowal**

⭐ Star this repository if you found it helpful!


