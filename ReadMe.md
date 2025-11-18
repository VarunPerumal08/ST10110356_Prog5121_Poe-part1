<p align="center">
  <img src="https://raw.githubusercontent.com/VarunPerumal08/ST10110356_Prog5121_Poe-part1/main/AppLogo.jpg" width="320" alt="QuizPulse Logo"/>
</p>

<h1 align="center">🌐 QuizPulse</h1>

<p align="center">
  <strong>A modern, intelligent, and beautifully designed quiz application built with Kotlin & Firebase.</strong><br/>
  <em>Featuring biometric authentication, multilingual support, dynamic difficulty, leaderboard, notifications, and real-time data updates.</em>
</p>

---

<!-- BANNER -->
<img src="https://dummyimage.com/1200x180/0066ff/ffffff&text=+🚀+Welcome+to+QuizPulse+" width="100%"/>

---

# 📘 Table of Contents
> *Click to jump to any section instantly.*

- [✨ Features](#-features)
- [🖼️ Screenshots](#️-screenshots)
- [🎯 Purpose of the Application](#-purpose-of-the-application)
- [🎨 Design Considerations](#-design-considerations)
- [🛠️ GitHub & GitHub Actions](#️-use-of-github--github-actions)
- [🧩 Tech Stack](#-tech-stack)
- [⚙️ Setup & Installation](#️-setup--installation)
- [🧠 How It Works](#-how-it-works)
- [🚀 App Release Status](#-app-release-status)
- [🌟 Future Improvements](#-future-improvements)
- [🤝 Contributors](#-contributors)
- [🪪 License](#-license)
- [🎥 Video Demonstration](#-video-demonstration)

---

# ✨ Features

## 🧑‍💻 User Authentication
- Email & Password registration  
- Google Sign-In (SSO)  
- Biometric Login (Fingerprint/Face Unlock)  
- Secure session management via Firebase Authentication  

## 🧠 Quiz System
- Multiple quiz categories  
- Difficulty levels: Easy & Hard  
- 3–5 questions per quiz  
- Instant scoring and feedback  
- Background music  
- Per-question countdown timer  

## 🏆 Leaderboard
- Tracks all attempts  
- Shows highest scores  
- Displays top users globally  
- Synced in real-time via Firestore  

## 🌍 Multilingual Support
Supported languages:  
🇬🇧 English | 🇿🇦 Afrikaans | 🇿🇦 isiZulu  

## 🔔 Real-Time Notifications
- Quiz reminders  
- New categories  
- System alerts  

---

<!-- BANNER -->
<img src="https://dummyimage.com/1200x160/007bff/ffffff&text=+🖼️+Screenshots+" width="100%"/>

---

# 🖼️ Screenshots

### 📌 Home Screen  
<p align="center">
  <img src="https://raw.githubusercontent.com/VarunPerumal08/ST10110356_Prog5121_Poe-part1/main/AppHome.jpg" width="300" height="400" />
</p>

### 📌 Sign Up Screen  
<p align="center">
  <img src="https://raw.githubusercontent.com/VarunPerumal08/ST10110356_Prog5121_Poe-part1/main/AppSignUp.jpg" width="300" height="400" />
</p>

### 📌 Login Screen  
<img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppLogin.jpg" width="300" height="400" />

### 📌 Select Quiz Screen  
<img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppSelectPage.jpg" width="300" height="400" />

### 📌 Leaderboard  
<img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppLeaderBoard.jpg" width="300" height="400" />

### 📌 Notifications  
<img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppNotification.jpg" width="300" height="400" />

### 📌 Settings Page  
<img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppSettings.jpg" width="300" height="400" />

---

<!-- BANNER -->
<img src="https://dummyimage.com/1200x160/0066ff/ffffff&text=+🎯+Purpose+of+the+Application+" width="100%"/>

---

# 🎯 Purpose of the Application
QuizPulse aims to make learning **fun, measurable, accessible, and engaging**.

### Why QuizPulse?
- Gamified learning environment  
- Measurable progress  
- Accessible with multilingual support  
- Personalized based on difficulty & user experience  
- Secure authentication  

---

# 🎨 Design Considerations

## 1️⃣ User Experience (UX)
- Clean layout  
- Intuitive navigation  
- High-contrast theming  
- Large, easy-to-tap buttons  
- Multilingual interface  
- Background audio effects  

## 2️⃣ Performance
- Optimized layouts  
- Cached assets  
- Kotlin coroutines  
- Efficient querying  

## 3️⃣ Security
- Firebase Authentication  
- Google SSO  
- Biometric login  
- Encrypted communication  

## 4️⃣ Scalability
- Modular architecture  
- Firebase autoscaling  
- Reusable UI & data components  

---

<!-- BANNER -->
<img src="https://dummyimage.com/1200x160/0077ff/ffffff&text=+🛠️+GitHub+%26+GitHub+Actions+" width="100%"/>

---

# 🛠️ Use of GitHub & GitHub Actions
GitHub was used for:
- Version control  
- Issue tracking  
- Code reviews  
- Documentation  

### Automated Testing Workflow

name: Android Unit Tests
on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]
jobs:
  unit-tests:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - uses: actions/setup-java@v3
      with:
        distribution: 'temurin'
        java-version: '17'
    - uses: actions/cache@v3
      with:
        path: |
          ~/.gradle/caches
          ~/.gradle/wrapper
        key: ${{ runner.os }}-gradle-${{ hashFiles('**/*.gradle*', '**/gradle-wrapper.properties') }}
    - run: chmod +x gradlew
    - run: ./gradlew test --stacktrace
🧩 Tech Stack
Component	Technology
Frontend	Kotlin
Authentication	Firebase Auth
Database	Firestore
Notifications	FCM
CI/CD	GitHub Actions
UI	XML Layouts

⚙️ Setup & Installation
1️⃣ Install Requirements
Android Studio

Firebase Project

Android SDK

Google Services JSON

2️⃣ Clone Repo
bash
Copy code
git clone https://github.com/ST10294145/QuizPulse.git
3️⃣ Run the App
Connect device → Build → Run

🧠 How It Works
🔐 Authentication
Email / Google SSO / Biometric

📚 Quiz Flow
Category → Difficulty → Timer → Answers → Score

🏆 Leaderboard
Live ranking via Firestore

🔔 Notifications
Automatic reminders with FCM

🚀 App Release Status
The app is complete and production-ready.
APK successfully generated.
Pending Google Play developer account approval.

🌟 Future Improvements
Dark mode

More languages

Achievement badges

Larger question bank

Animated transitions

🤝 Contributors
ST10294145 — Saihil Gurupersad

ST10311999 — Dinay Ramchander

ST10198206 — Nehara Pillay

ST10110356 — Varun Perumal

🪪 License
MIT License — free to use, modify, distribute.

<!-- BANNER --> <img src="https://dummyimage.com/1200x160/0066ff/ffffff&text=+🎥+Video+Demonstration+" width="100%"/>
🎥 Video Demonstration
<p align="center"> <a href="https://youtube.com/shorts/ujJWChi8kzQ?feature=share" target="_blank"> <img src="https://img.youtube.com/vi/ujJWChi8kzQ/0.jpg" alt="QuizePulse Video Preview" width="480"/> </a> </p>
