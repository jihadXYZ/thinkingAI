<div align="center">

# 🌾 HarvestGuard

### AI-Powered Post-Harvest Food Loss Prevention System

[![Next.js](https://img.shields.io/badge/Next.js-16-2E7D32?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-2E7D32?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-4.0-2E7D32?style=for-the-badge&logo=tailwindcss)](https://tailwindcss.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Auth-2E7D32?style=for-the-badge&logo=firebase)](https://firebase.google.com/)
[![Python](https://img.shields.io/badge/Python-Flask-2E7D32?style=for-the-badge&logo=python)](https://flask.palletsprojects.com/)

</div>

---

## 📋 About The Project

**HarvestGuard** is an intelligent agricultural solution designed to help Bangladeshi farmers reduce post-harvest crop losses through AI-powered disease detection, real-time weather forecasting, and smart storage recommendations.

> 🌱 **Problem**: Bangladesh loses approximately 30% of harvested crops annually due to improper storage, pest attacks, and environmental factors.

> 🌿 **Solution**: HarvestGuard provides farmers with AI-driven insights to identify crop diseases, predict weather patterns, and receive actionable storage guidance.

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🔬 **AI Crop Scanner** | Upload or capture crop images for instant disease detection using TensorFlow ML models |
| 🌦️ **Weather Forecasting** | 7-day weather predictions with agricultural impact analysis and alerts |
| 📊 **Smart Dashboard** | Personalized recommendations, scan history, and crop health tracking |
| 🌐 **Multi-language** | Full Bengali and English language support |
| 🔐 **Authentication** | Secure Firebase authentication system |

---

## 🛠️ Technologies Used

### Frontend
- **Next.js 16** - React framework with App Router
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS 4** - Utility-first styling
- **shadcn/ui** - UI component library
- **Lucide React** - Icon library

### Backend & Services
- **Firebase** - Authentication & Firestore database
- **Flask (Python)** - AI model server
- **TensorFlow** - ML for crop disease detection
- **OpenWeatherMap API** - Weather data

---

## 📁 Project Structure

\`\`\`
harvestguard/
├── app/
│   ├── page.tsx              # Landing page
│   ├── scanner/              # AI crop scanner
│   ├── dashboard/            # User dashboard
│   ├── weather/              # Weather forecasting
│   ├── login/                # Authentication
│   └── api/                  # API routes
├── components/               # Reusable UI components
├── lib/                      # Utilities & Firebase config
└── public/                   # Static assets
\`\`\`

---

## 🚀 Installation & Setup

### Prerequisites
- Node.js 18+
- Python 3.8+ (for Flask server)
- Firebase account

### Steps

\`\`\`bash
# 1. Clone the repository
git clone https://github.com/your-repo/harvestguard.git
cd harvestguard

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env.local
# Add your Firebase and OpenWeather API keys

# 4. Run the development server
npm run dev

# 5. (Optional) Start Flask AI server
cd flask-server
pip install -r requirements.txt
python app.py
\`\`\`

---

## 👥 Team Members

| Name | ID | Role | Responsibilities |
|------|-----|------|------------------|
| **Akram Rafid** | 231017512 | Full-Stack Developer | Built responsive UI with Next.js & Tailwind CSS. Implemented API routes for crop recognition & weather data. Integrated Firebase Firestore for data persistence. Developed dashboard analytics, scan history features, and data export functionality. |
| **Jihad Hossain Jisan** | 231016712 | AI & Backend Engineer | Developed TensorFlow ML model for crop disease detection. Built Flask server for AI inference. Implemented Firebase Authentication with secure login/registration. Created API endpoints for image processing and weather integration. |
| **Zarin Tasnim** | 231016312 | UI/UX Designer & Media | Designed complete visual identity and brand guidelines. Created wireframes and prototypes. Produced project demo video and documentation visuals. Ensured consistent design language and mobile responsiveness across all pages. |

---

## 📄 License

This project is developed for academic purposes.

---

<div align="center">

**🌾 Built with 💚 for Bangladeshi Farmers 🌾**

*আপনার ফসল বাঁচান, ভবিষ্যৎ গড়ুন*

</div>
