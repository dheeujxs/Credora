🚀 AI SaaS Finance Platform

A modern AI-powered finance platform built with the MERN stack, integrated with Google Gemini AI API for intelligent insights, Cloudinary for media storage, and deployed seamlessly on Render.

✨ Features

🔐 User Authentication – Secure signup/login with JWT

📊 Finance Management – Track income, expenses, and investments

🤖 AI-Powered Insights – Gemini API for smart recommendations & analytics

☁️ Cloudinary Integration – Store & manage profile images & receipts

🌐 Deployment – Backend hosted on Render, frontend on Vercel/Netlify

🛠️ Tech Stack

Frontend: React + TailwindCSS

Backend: Node.js + Express.js

Database: MongoDB Atlas

AI Integration: Google Gemini API

File Storage: Cloudinary

Deployment: Render (Backend), Vercel/Netlify (Frontend)

📦 Installation
1. Clone the Repository
git clone https://github.com/your-username/ai-saas-finance.git
cd ai-saas-finance

2. Setup Backend
cd backend
npm install

Create .env file
PORT=5000
MONGO_URI=your_mongo_connection
JWT_SECRET=your_secret_key

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Gemini AI
GEMINI_API_KEY=your_gemini_api_key


Run backend:

npm start

3. Setup Frontend
cd ../frontend
npm install

Create .env file
VITE_BACKEND_URL=https://your-backend.onrender.com


Run frontend:

npm run dev

🚀 Deployment
Backend (Render)

Push code to GitHub

Connect repo to Render

Add environment variables in Render dashboard

Deploy 🎉

Frontend (Vercel/Netlify)

Connect repo to Vercel/Netlify

Add environment variable:

VITE_BACKEND_URL=https://your-backend.onrender.com


Deploy 🎉

🤖 AI with Gemini API

Example request:

import fetch from "node-fetch";

const response = await fetch("https://generativelanguage.googleapis.com/v1/models/gemini-pro:generateText?key=" + process.env.GEMINI_API_KEY, {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({
    prompt: { text: "Give me financial advice for saving money." }
  })
});

const data = await response.json();
console.log(data);

📸 Cloudinary Upload Example
import { v2 as cloudinary } from "cloudinary";

cloudinary.config({
  cloud_name: process.env.CLOUDINARY_CLOUD_NAME,
  api_key: process.env.CLOUDINARY_API_KEY,
  api_secret: process.env.CLOUDINARY_API_SECRET,
});

const uploadImage = async (filePath) => {
  const result = await cloudinary.uploader.upload(filePath, {
    folder: "finance-platform",
  });
  return result.secure_url;
};

🧑‍💻 Contributing

Pull requests are welcome! For major changes, open an issue first to discuss.
