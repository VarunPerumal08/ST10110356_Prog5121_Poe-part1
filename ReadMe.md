<p align="center">
  <img src="https://raw.githubusercontent.com/VarunPerumal08/ST10110356_Prog5121_Poe-part1/main/AppLogo.jpg" width="220" alt="QuizPulse Logo"/>
</p>

<h1 align="center">📱 QuizPulse</h1>


QuizPulse is an interactive and modern quiz application built using Kotlin and Android Studio, designed to provide an enjoyable and customizable learning experience.
The app integrates Firebase Authentication, Firestore Database, Cloud Messaging, biometric login, multilingual support, and advanced user-defined features such as difficulty levels, leaderboard, background music, timers, and more.

## 🚀 Table of Contents

Features

Screenshots

App Purpose & Design Considerations

GitHub & GitHub Actions Usage

Tech Stack

Setup & Installation

How It Works

Future Improvements

Contributors

License

## 🚀 Features


### 🧑‍💻 User Authentication

Email & Password registration

Google Sign-In (SSO)

Biometric Login (Fingerprint/Face Unlock)

Secure session management using Firebase Authentication

### 🧠 Quiz System

✔ Multiple quiz categories

✔ 3–5 questions per quiz depending on difficulty

✔ Instant scoring + feedback

✔ Difficulty levels:

Easy

Hard

✔ Background music to improve the user experience

✔ Countdown Timer per question

(Improves challenge + prevents guessing)

### 🏆 Leaderboard & Scoreboard

Stores all quiz attempts

Shows highest scores

Displays top players globally

Synced in real-time using Firebase Firestore

### 🌍 Multilingual Support

QuizPulse now supports:

English

Afrikaans

isiZulu

The language can be changed in the settings screen.

### 🔔 Real-Time Notifications

Using Firebase Cloud Messaging (FCM), users receive:

Quiz reminders

New category releases

Special updates

System alerts

UI assets and themes are being prepared for the next release.

## 🖼️ Screenshots

### 📌 Home Screen  

<p align="center">
  <img src="https://raw.githubusercontent.com/VarunPerumal08/ST10110356_Prog5121_Poe-part1/main/AppHome.jpg" width="300" height="400" />
</p>

### 📌 Sign Up Screen 

<p align="center">
  <img src="https://raw.githubusercontent.com/VarunPerumal08/ST10110356_Prog5121_Poe-part1/main/AppSignUp.jpg" width="300" height="400" />
</p>

📌 Login Screen  
<p align="left">
  <img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppLogin.jpg" width="300" height="400" />
</p>

📌 Select Quiz Screen  
<p align="left">
  <img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppSelectPage.jpg" width="300" height="400" />
</p>

📌 Leaderboard  
<p align="left">
  <img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppLeaderBoard.jpg" width="300" height="400" />
</p>

📌 Notifications  
<p align="left">
  <img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppNotification.jpg" width="300" height="400" />
</p>

📌 Settings Page  
<p align="left">
  <img src="https://raw.githubusercontent.com/ST10294145/QuizePulse/main/AppSettings.jpg" width="300" height="400" />
</p>

## 📘 Purpose of the Application

QuizPulse was developed as a modern, interactive quiz platform designed to make learning engaging, accessible, and measurable. The application combines gamification techniques with educational value, giving users a motivating environment to test and expand their knowledge.

### The purpose of QuizPulse includes:

✅ Enhancing learning through gamification

The app uses quizzes, scoring, feedback, and leaderboards to make learning fun and competitive.

✅ Providing measurable progress

Users can track improvements over time through score history, leaderboards, and difficulty settings.

✅ Supporting multilingual accessibility

With English, isiZulu, and Afrikaans support, the app caters to a wider South African audience.

✅ Offering personalized experiences

Users can choose difficulty levels, receive real-time notifications, and listen to background audio enhancements during quizzes.

✅ Enabling secure authentication and personalization

Through Firebase Authentication, Google Sign-In, and biometric login, users experience a secure, modern login flow.

QuizPulse ultimately aims to blend education and entertainment into a seamless mobile learning tool that grows with the user’s skill and engagement.

## 🧩 Design Considerations

The app design follows best practices in UX, performance, security, and scalable architecture to ensure reliability and a smooth user experience.

### 1. User Experience (UX)

Clean, minimal layout with intuitive navigation

High-contrast color themes for readability

Large, easily tappable buttons for accessibility

Simple category selection and interactive quiz flow

Consistent screen layouts across devices

Multi-language support integrated into the UI

Background music and sound effects to enhance engagement

### 2. Performance

Firebase Realtime Database allows fast, lightweight data retrieval

Kotlin coroutines used for non-blocking operations

Images and assets cached locally to improve loading speeds

Efficient state management to reduce unnecessary recomputations

Optimized layouts using ConstraintLayout and proper view hierarchy

Timer and background processes optimized for minimal CPU usage

### 3. Security

Firebase Authentication ensures secure credential management

Google Sign-In with token validation

Biometric authentication (fingerprint) for enhanced login security

Encrypted data transmission via HTTPS

Secure password recovery and credential update flows

Firebase rules applied to prevent unauthorized data access

### 4. Scalability

Firebase backend automatically scales with user growth

Realtime Database supports large volumes of concurrent reads/writes

Cloud Messaging supports mass notification delivery

Modular Kotlin architecture enables easy updates (e.g., new categories, languages, or themes)

Separation of concerns (UI, logic, data layers) improves maintainability

## 🛠️ Use of GitHub & GitHub Actions

GitHub and GitHub Actions played a critical role in the development and maintenance of QuizPulse.

🔹 GitHub Usage

GitHub was used extensively to streamline collaborative development, maintain code quality, and provide transparent version history.

Key uses include:

✔ Version Control

Every change was tracked using commits, allowing rollback and history auditing.

✔ Branching & Merging

Each team member worked in isolated feature branches

Work was merged via Pull Requests

Ensured safe integration without breaking main code

✔ Issue Tracking

GitHub Issues were used to:

Document bugs

Track new features

Assign tasks to team members

Monitor project progress

✔ Documentation Hosting

The README and other documentation files were hosted directly in the GitHub repository for easy access and updates.

✔ Collaborative Development

Team members collaborated through:

Code reviews

Inline comments

Pull Request discussions

This ensured consistent quality and shared understanding of the project structure.

## 🔹 GitHub Actions: Unit Test Workflow

To ensure the reliability and stability of QuizPulse, a dedicated GitHub Actions workflow for automated unit testing was implemented.
This workflow runs every time a commit is pushed to the main branch or when a Pull Request is opened.
It ensures that all test cases pass before new code is merged, reducing bugs and preventing regressions.

### ✅ Purpose of the Workflow

The Unit Test workflow was added to:

Automatically verify core logic after every change

Prevent broken code from being merged into main

Maintain consistent code quality

Give early feedback to developers during the CI/CD pipeline

Ensure that quiz logic, authentication flows, and utility functions behave as expected

### 🧪 What the Workflow Does

This GitHub Action:

Checks out the repository

Sets up Java 17 (required for Android builds)

Caches Gradle for faster runs

Grants execution permission to gradlew

Executes the full suite of unit tests using:

./gradlew test --stacktrace

### 📄 Unit Test Workflow Code

Add this directly under your GitHub Actions section:

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
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Set up JDK 17
        uses: actions/setup-java@v3
        with:
          distribution: 'temurin'
          java-version: '17'

      - name: Cache Gradle
        uses: actions/cache@v3
        with:
          path: |
            ~/.gradle/caches
            ~/.gradle/wrapper
          key: ${{ runner.os }}-gradle-${{ hashFiles('**/*.gradle*', '**/gradle-wrapper.properties') }}
          restore-keys: |
            ${{ runner.os }}-gradle-

      - name: Grant execute permission for Gradle
        run: chmod +x gradlew

      - name: Run Unit Tests
        run: ./gradlew test --stacktrace

### 🧩 Why This Matters

Including automated unit testing in the CI/CD pipeline:

Ensures high project stability

Reduces manual testing time

Prevents defects from reaching production

Helps maintain clean, reliable code

Supports continuous integration best practices

This workflow contributes significantly to the scalability, robustness, and long-term maintainability of the QuizPulse application.


## 🧩 Tech Stack
Component	Technology
Frontend	Kotlin (Android Studio)
Authentication	Firebase Authentication
Database	Firebase Firestore
Notifications	Firebase Cloud Messaging
UI Design	XML Layouts
Version Control	Git + GitHub
CI/CD	GitHub Actions

## ⚙️ Setup & Installation
Prerequisites

Android Studio (latest)

Firebase Project

Android SDK

Google Services JSON file

Git (recommended)

Running the App
git clone https://github.com/ST10294145/QuizPulse.git

Open project in Android Studio

Connect device or emulator

Run the project

## 🧠 How It Works

### 🔐 Authentication

Register via email or Google SSO

Optional: biometric unlock

### 📚 Quiz

Select category

Select difficulty

Timer starts

Answer questions

Receive scoring instantly

### 🏆 Leaderboard

Scores saved automatically

Global ranking updates live

### 🔔 Notifications

Reminders and new updates pushed via FCM

## 📦 App Release Status

Although the QuizPulse application has not yet been published to the Google Play Store due to administrative and technical issues with the developer account, the app is fully developed and production-ready.
An APK build has been successfully generated, demonstrating that:

The application compiles without errors

All core features function as intended

The app is stable and ready for deployment

Only the final publishing step is pending

Once the Google Play developer account is resolved, QuizPulse can be uploaded immediately for public release.

### 🧪 Future Improvements

Full Dark Mode

More languages

Achievement badges

Larger question database

Animated transitions

## 🤝 Contributors

ST10294145 — Saihil Gurupersad

ST10311999 — Dinay Ramchander

ST10198206 — Nehara Pillay

ST10110356 — Varun Perumal

### 🪪 License

MIT License — free to use, modify, and distribute.

## 🎥 Video Demonstration

Add your YouTube link here once uploaded.
