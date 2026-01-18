# AI Thumbnail Generator

A full-stack MERN application for generating high-quality, YouTube-ready thumbnails using AI.  
The platform supports text-to-image and image-to-image generation, prompt enhancement using AI, Cloudinary-based image hosting, and complete user generation history management.

---

## 🚀 Features

### 🌐 Frontend (React + Vite)
- Modern UI built with **React**, **TailwindCSS**, **Zustand**, and **Vite**
- Multi-step thumbnail generation workflow
- Text-based and image-based thumbnail generation
- AI prompt enhancement toggle
- Customizable filters (category, mood, theme, color, text style, etc.)
- Template-based thumbnail selection
- Results preview with individual & bulk download (ZIP)
- User generation history with search & filter support
- Responsive design for all screen sizes

---

### 🛠️ Backend (Node.js + Express)
- RESTful API architecture
- AI prompt enhancement using **OpenAI**
- Image generation using **Google Gemini**
- Cloudinary integration for secure image storage
- MongoDB for storing user data and generation history
- File uploads handled with Multer
- JWT-based authentication (if enabled)
- Robust error handling and validation

---

## 🏗️ Workflow Overview

1. **User Input**
   - Selects generation mode (text or image)
   - Provides prompt or uploads an image
   - Chooses optional AI enhancement
   - Selects filters and visual style/template

2. **Frontend Processing**
   - State managed via Zustand (`uiStore`, `imageStore`)
   - Input validation before API request

3. **Backend Processing**
   - Enhances prompt (optional) using OpenAI
   - Generates thumbnails using Google Gemini
   - Uploads results to Cloudinary
   - Stores generation metadata in MongoDB

4. **Results & History**
   - Displays generated thumbnails
   - Allows downloads and history management

---

## 📦 Technology Stack

### Frontend
- React
- Vite
- TailwindCSS
- Zustand
- Axios
- JSZip
- Lucide Icons

### Backend
- Node.js
- Express.js
- MongoDB + Mongoose
- Google Gemini AI
- OpenAI API
- Cloudinary
- Multer
- JWT Authentication
- dotenv, cors, bcryptjs

---

## 📝 Example API Usage

### Generate Thumbnail from Prompt
```http
POST /api/generate
Content-Type: application/json

{
  "prompt": "A bold tech thumbnail with neon colors",
  "enhancePrompt": true,
  "category": "Technology",
  "mood": "Excited"
}
