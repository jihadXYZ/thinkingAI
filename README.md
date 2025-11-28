# HarvestGuard - আপনার ফসল বাঁচান, ভবিষ্যৎ গড়ুন

<div align="center">

![HarvestGuard Logo](public/icon.svg)

**Protect Your Harvest. Secure Your Future.**

*An intelligent agricultural platform designed to help Bangladesh's farmers reduce post-harvest food loss through AI-powered disease detection, real-time weather alerts, and smart crop management.*

[![Next.js](https://img.shields.io/badge/Next.js-16.0-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.2-blue?style=for-the-badge&logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.1-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Latest-orange?style=for-the-badge&logo=firebase)](https://firebase.google.com/)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [Project Architecture](#project-architecture)
- [Installation & Setup](#installation--setup)
- [Environment Variables](#environment-variables)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Team Members](#team-members)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

**HarvestGuard** is a comprehensive web application built to address the critical issue of post-harvest food loss in Bangladesh, where approximately **30% of crops are lost** due to inadequate storage, unpredictable weather, and crop diseases. Our platform empowers farmers with:

- AI-powered crop disease detection using image recognition
- Real-time weather forecasting and alerts
- Smart crop batch management and tracking
- Risk assessment and protection recommendations
- Bilingual support (Bengali/English) for accessibility

---

## Problem Statement

> **"বাংলাদেশে ৩০% ফসল নষ্ট হয়। We can change that."**

Post-harvest losses significantly impact millions of farmers' livelihoods in Bangladesh. Irregular weather patterns and lack of timely information lead to substantial crop damage. HarvestGuard bridges this gap by providing:

- Early warning systems for weather hazards
- Disease identification before it spreads
- Data-driven storage recommendations
- Actionable insights in the farmer's native language

---

## Key Features

### 1. AI-Powered Disease Detection (Scanner)
- **Camera/Upload Integration**: Capture or upload images of crop leaves
- **Real-time Analysis**: AI model identifies diseases like bacterial leaf blight, brown spot, late blight, powdery mildew, and more
- **Comprehensive Reports**: Detailed symptoms, causes, remedies, and prevention tips
- **Treatment Options**: Both organic and chemical treatment recommendations
- **Bilingual Results**: All information available in Bengali and English

### 2. Weather Forecasting & Alerts
- **7-Day Forecast**: Accurate weather predictions using OpenWeather API
- **Real-time Data**: Current temperature, humidity, wind speed, UV index
- **Location-based**: GPS auto-detection or manual location selection
- **Weather Alerts**: Notifications for rain, storms, extreme heat
- **Crop Protection Advice**: Weather-specific recommendations for each crop type

### 3. Crop Management Dashboard
- **Batch Tracking**: Monitor multiple crop batches simultaneously
- **Risk Assessment**: Automatic risk level calculation (low/medium/high)
- **Storage Recommendations**: Optimal storage type suggestions
- **Export Functionality**: Download data as CSV or JSON
- **Gamification**: Achievement badges for successful harvests

### 4. User Authentication
- **Secure Registration/Login**: Firebase-powered authentication
- **Password Hashing**: SHA-256 encryption for security
- **Persistent Sessions**: LocalStorage-based session management
- **Profile Management**: User preferences and language settings

---

## Technologies Used

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| **Next.js** | 16.0.3 | React framework with App Router, Server Components |
| **React** | 19.2.0 | UI component library |
| **TypeScript** | 5.x | Type-safe JavaScript |
| **Tailwind CSS** | 4.1.9 | Utility-first CSS framework |
| **shadcn/ui** | Latest | Accessible UI component library |
| **Recharts** | Latest | Data visualization and charts |
| **Lucide React** | 0.454.0 | Icon library |

### Backend & Services
| Technology | Purpose |
|------------|---------|
| **Firebase Firestore** | NoSQL database for user data and crop records |
| **Firebase Authentication** | User authentication infrastructure |
| **OpenWeather API** | Weather data and forecasting |
| **Flask (Python)** | AI/ML server for crop disease recognition |
| **Vercel** | Deployment and hosting platform |

### AI & Machine Learning
| Technology | Purpose |
|------------|---------|
| **TensorFlow/PyTorch** | Deep learning framework for disease detection |
| **Flask Server** | REST API for ML model inference |
| **Image Classification** | CNN-based crop disease identification |

### Development Tools
| Tool | Purpose |
|------|---------|
| **pnpm** | Package manager |
| **ESLint** | Code linting |
| **PostCSS** | CSS processing |
| **Vercel Analytics** | Performance monitoring |

---

## Project Architecture

\`\`\`
harvestguard/
├── app/                          # Next.js App Router pages
│   ├── api/                      # API route handlers
│   │   ├── crop-recognize/       # AI disease detection proxy
│   │   └── weather/              # Weather data fetching
│   ├── dashboard/                # User dashboard
│   ├── login/                    # Authentication - login
│   ├── register/                 # Authentication - registration
│   ├── scanner/                  # AI crop disease scanner
│   ├── weather/                  # Weather forecasting page
│   ├── layout.tsx                # Root layout with providers
│   ├── page.tsx                  # Landing page
│   └── globals.css               # Global styles & design tokens
├── components/                   # Reusable React components
│   ├── ui/                       # shadcn/ui components
│   ├── landing/                  # Landing page sections
│   ├── header.tsx                # Navigation header
│   └── footer.tsx                # Site footer
├── lib/                          # Utility functions & contexts
│   ├── firebase.ts               # Firebase configuration
│   ├── language-context.tsx      # i18n language provider
│   ├── data-context.tsx          # Global state management
│   ├── bangladesh-locations.ts   # Location data for Bangladesh
│   └── utils.ts                  # Helper utilities
├── hooks/                        # Custom React hooks
├── public/                       # Static assets
└── styles/                       # Additional stylesheets
\`\`\`

---

## Installation & Setup

### Prerequisites

- **Node.js** >= 18.0.0
- **pnpm** (recommended) or npm/yarn
- **Python** >= 3.8 (for Flask AI server)
- **Firebase Account** (for database)
- **OpenWeather API Key** (for weather data)

### Step 1: Clone the Repository

\`\`\`bash
git clone https://github.com/your-username/harvestguard.git
cd harvestguard
\`\`\`

### Step 2: Install Dependencies

\`\`\`bash
# Using pnpm (recommended)
pnpm install

# Or using npm
npm install

# Or using yarn
yarn install
\`\`\`

### Step 3: Firebase Setup

1. Create a new Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable **Firestore Database** in your project
3. Configure Firestore Security Rules (see `firestore.rules` file)
4. Copy your Firebase configuration to `lib/firebase.ts`

> **Note:** Refer to `FIREBASE_SETUP.md` for detailed Firebase configuration instructions.

### Step 4: Flask AI Server Setup (Optional)

The AI disease detection requires a separate Flask server:

\`\`\`bash
# Navigate to the Flask server directory
cd flask-server

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install Python dependencies
pip install -r requirements.txt

# Run the Flask server
python app.py
\`\`\`

The Flask server will run on `http://localhost:5000` by default.

---

## Environment Variables

Create a `.env.local` file in the root directory:

\`\`\`env
# OpenWeather API
OPENWEATHER_API_KEY=your_openweather_api_key

# Flask AI Server URL (optional - defaults to localhost:5000)
FLASK_SERVER_URL=http://localhost:5000

# Firebase Configuration (already configured in lib/firebase.ts)
# If you want to override:
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
\`\`\`

### Getting API Keys

1. **OpenWeather API**: Sign up at [OpenWeatherMap](https://openweathermap.org/api) for a free API key
2. **Firebase**: Get configuration from Firebase Console > Project Settings

---

## Running the Application

### Development Mode

\`\`\`bash
# Start the Next.js development server
pnpm dev
# or
npm run dev

# The app will be available at http://localhost:3000
\`\`\`

### Production Build

\`\`\`bash
# Build the application
pnpm build

# Start production server
pnpm start
\`\`\`

### Running All Services

For full functionality, run both servers:

\`\`\`bash
# Terminal 1: Next.js frontend
pnpm dev

# Terminal 2: Flask AI server (if using disease detection)
cd flask-server && python app.py
\`\`\`

---

## API Endpoints

### Weather API
\`\`\`
GET /api/weather?lat={latitude}&lng={longitude}&location={name}
\`\`\`
Returns current weather and 7-day forecast for the specified location.

### Crop Recognition API
\`\`\`
POST /api/crop-recognize
Content-Type: multipart/form-data
Body: { image: File }
\`\`\`
Analyzes crop leaf images and returns disease detection results.

\`\`\`
GET /api/crop-recognize
\`\`\`
Health check endpoint for the AI server connection status.

---

## Team Members

### Akram Rafid
**Student ID:** 231017512  
**Role:** Full-Stack Developer (Frontend & Backend)

**Responsibilities:**
- Designed and implemented the complete **frontend architecture** using Next.js 16 and React 19
- Built responsive UI components with **Tailwind CSS** and **shadcn/ui** component library
- Developed the **Dashboard page** with crop batch management, risk assessment, and data visualization
- Implemented the **Weather forecasting page** with real-time data integration and location services
- Created the **Landing page** with hero section, features showcase, and testimonials
- Set up **API route handlers** for weather data and AI server communication
- Implemented **global state management** using React Context API
- Configured **bilingual support** (Bengali/English) with language context provider
- Built **data export functionality** (CSV/JSON) for crop records
- Integrated **Vercel Analytics** for performance monitoring
- Ensured **mobile-first responsive design** across all pages

---

### Jihad Hossain Jisan
**Student ID:** 231016712  
**Role:** AI/ML Engineer & Backend Developer

**Responsibilities:**
- Developed the **AI-powered crop disease detection system** using deep learning models
- Built and deployed the **Flask server** for ML model inference
- Trained the **image classification model** on crop disease datasets (rice, wheat, tomato, potato)
- Implemented the **disease database** with comprehensive information including:
  - Disease symptoms and causes
  - Organic and chemical treatment options
  - Prevention strategies
  - Risk severity and spread assessment
- Created the **Scanner page** with camera integration and image upload functionality
- Integrated the **OpenWeather API** for real-time weather data
- Set up **Firebase Firestore** database for user data persistence
- Implemented **user authentication system** with:
  - Secure registration and login flows
  - Password hashing using SHA-256
  - Session management with localStorage
- Developed **security rules** for Firestore database
- Created API endpoints for communication between frontend and AI server
- Wrote technical documentation for Firebase setup and AI server deployment

---

### Zarin Tasnim
**Student ID:** 231016312  
**Role:** UI/UX Designer & Creative Lead

**Responsibilities:**
- Designed the complete **visual identity** and **brand guidelines** for HarvestGuard
- Created the **color system** with agricultural-themed palette:
  - Primary green for growth and sustainability
  - Weather-specific colors (sun, rain, storm indicators)
  - Risk level indicators (low/medium/high)
- Designed **typography system** using Lexend and Hind Siliguri (Bengali) fonts
- Created **custom CSS animations** including:
  - Float animation for icons
  - Weather bounce effects
  - Pulse glow for alerts
- Designed the **landing page layout** with:
  - Hero section with background video
  - Features cards with interactive elements
  - Testimonial carousel
  - Call-to-action sections
- Created **mobile-responsive layouts** for all screen sizes
- Designed **card-based UI patterns** for dashboard and scanner pages
- Selected and curated **iconography** using Lucide React icons
- Created **promotional video content** for the application
- Captured and edited **photography/imagery** for:
  - Landing page backgrounds
  - Login/Register page backgrounds
  - Placeholder images and assets
- Designed **badge system** for gamification elements
- Ensured **accessibility standards** (WCAG) compliance
- Created **user flow diagrams** and wireframes
- Designed **error states** and loading animations

---

## Screenshots

### Landing Page
The hero section features a dynamic background video showcasing Bangladesh's agricultural heritage, with bilingual call-to-action buttons.

### Dashboard
Clean, card-based interface showing active crop batches, success rates, and quick statistics with risk indicators.

### Disease Scanner
Camera-enabled interface for capturing crop images, with detailed AI analysis results including treatment recommendations.

### Weather Forecast
Location-aware weather dashboard with 7-day forecast, current conditions, and crop-specific protection advice.

---

## Contributing

We welcome contributions to HarvestGuard! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## License

This project was developed as part of an academic project. All rights reserved.

---

<div align="center">

**HarvestGuard** - Empowering Bangladesh's Farmers with Technology

*আপ��ার ফসল বাঁচান, ভবিষ্যৎ গড়ুন*

Made with ❤️ by Team HarvestGuard

</div>
