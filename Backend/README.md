# KoowalAI ChatBot - Backend

Node.js/Express backend API for the KoowalAI ChatBot application.

## Tech Stack

- **Node.js** - Runtime Environment
- **Express 5** - Web Framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **Clerk SDK** - Authentication Middleware
- **ImageKit** - Image Storage

## Quick Start

```bash
# Install dependencies
npm install

# Start server
node index.js

# Start with auto-reload (development)
npx nodemon index.js
```

## Environment Variables

Create a `.env` file in the Backend directory:

```env
PORT=5000
CLIENT_URL=http://localhost:5173
MONGODB_URI=mongodb+srv://your-connection-string
CLERK_SECRET_KEY=sk_test_xxxxx
CLERK_PUBLISHABLE_KEY=pk_test_xxxxx
IMAGEKIT_PUBLIC_KEY=public_xxxxx
IMAGEKIT_PRIVATE_KEY=private_xxxxx
IMAGEKIT_URL_ENDPOINT=https://ik.imagekit.io/your-id
```

## API Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| `GET` | `/api/upload` | ImageKit auth params | ❌ |
| `POST` | `/api/chat` | Create new chat | ✅ |
| `GET` | `/api/userChats` | Get user's chats | ✅ |
| `GET` | `/api/chat/:id` | Get chat by ID | ✅ |
| `PUT` | `/api/chat/:id` | Update chat | ✅ |

## Database Models

- **Chat** - Individual chat conversations with history
- **UserChats** - User's chat list with titles

