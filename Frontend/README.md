# KoowalAI ChatBot - Frontend

React-based frontend for the KoowalAI ChatBot application.

## Tech Stack

- **React 19** - UI Framework
- **Vite** - Build Tool & Dev Server
- **React Router 7** - Client-side Routing
- **TanStack Query** - Server State Management
- **Clerk React** - Authentication
- **Google Generative AI** - Gemini Integration
- **React Markdown** - AI Response Rendering
- **ImageKit React** - Image Upload

## Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Environment Variables

Create a `.env` file in the Frontend directory:

```env
VITE_API_ENDPOINT=http://localhost:5000
VITE_CLERK_PUBLISHABLE_KEY=pk_test_xxxxx
VITE_GEMINI_KEY=AIzaSyxxxxx
VITE_IK_ENDPOINT=https://ik.imagekit.io/your-id
VITE_IK_PUBLIC_KEY=public_xxxxx
```

## Project Structure

```
src/
├── Components/     # Reusable UI components
├── Layouts/        # Page layout wrappers
├── Lib/            # Utilities & configurations
├── Routes/         # Page components
├── App.jsx         # Route configuration
└── main.jsx        # Entry point
```
