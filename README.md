# Spotify Aura – GenAI Music Discovery Prototype

![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Build-Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Vercel](https://img.shields.io/badge/Deploy-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Prototype-brightgreen?style=for-the-badge)

## Overview

**Spotify Aura** is an unofficial Spotify-inspired GenAI product prototype built for personalized music discovery. The prototype demonstrates how a music platform could convert a user's mood, intent, social context, and listening preferences into an adaptive AI-generated listening session.

The product is designed as a **Vercel-ready React + Vite frontend**. It focuses on product thinking, user experience, GenAI interaction flow, privacy controls, and a believable Spotify-like mobile interface.

> This is a static/simulated prototype. It does not use the real Spotify API, real user accounts, or real personal data.

---

## Problem Statement Analysis

Modern music platforms already recommend songs, but most recommendation systems still feel passive. Users often need to search manually, skip repeatedly, or rely on generic playlists that do not fully understand their current situation.

Spotify Aura explores a more active recommendation experience:

- The user describes their mood or situation in natural language.
- The AI generates a listening session based on that prompt.
- The session adapts through trust, memory, and feedback controls.
- A group mode blends multiple listeners into one shared Jam session.

The goal is not just to show a music UI. The goal is to show how GenAI can become a product layer on top of recommendation systems.

---

## What Judges / Evaluators Will Care About

1. **Clear product problem**  
   The prototype must solve a real discovery problem, not just copy Spotify's existing interface.

2. **GenAI relevance**  
   GenAI should be central to the experience through prompt-based session creation, mood interpretation, and group blending.

3. **User trust and privacy**  
   Music personalization can feel invasive. The project includes controls for memory, explanation, and trust.

4. **Usable prototype**  
   A judge should be able to open the deployed link and understand the flow without explanation.

5. **Vercel deployment readiness**  
   The repository must install, build, and deploy cleanly.

6. **Submission clarity**  
   README, run commands, and deployment steps must be obvious.

---

## Core Features

### 1. Prompt-to-Session AI Flow

Users can enter prompts such as:

```txt
Make me a calm focus session for late-night study.
```

The prototype converts the prompt into a personalized listening session with a title, vibe, tracks, and AI reasoning.

### 2. Spotify-Like Mobile Interface

The UI is designed around a premium music-app experience:

- dark theme
- mobile-first layout
- playlist/session cards
- now-playing panel
- smooth section switching
- modern gradients and spacing

### 3. Group Jam Agent

The Group Jam Agent simulates a shared listening experience where multiple users' moods and preferences are blended into one queue.

Example use cases:

- friends studying together
- gym group playlist
- road trip music
- party warm-up session

### 4. Trust and Memory Controls

The prototype includes user-facing controls for:

- AI memory on/off
- explanation of why songs were selected
- privacy-safe personalization
- user control over future recommendations

### 5. Simulated AI Output

The project uses simulated/static AI responses so that it can run without backend cost, API keys, Spotify login, or database setup.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React |
| Build Tool | Vite |
| Styling | CSS / Tailwind-style utility classes depending on implementation |
| Icons | Lucide React |
| Deployment | Vercel |
| Backend | Not required for prototype |
| External APIs | Not used |

---

## Project Structure

```txt
Spotify_AI/
│
├── src/
│   ├── App.jsx / App.js
│   ├── main.jsx / main.js
│   └── styles or component files
│
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
├── vercel.json
├── .gitignore
└── README.md
```

The exact file names may vary slightly depending on the final pushed version, but the project follows a standard Vite React structure.

---

## Installation and Local Setup

### Prerequisites

Install Node.js first.

Recommended:

```txt
Node.js 20 LTS or newer
npm 10 or newer
```

Check your versions:

```bash
node -v
npm -v
```

---

### Step 1: Clone the Repository

```bash
git clone https://github.com/satyam9140/Spotify_AI.git
```

Go inside the project folder:

```bash
cd Spotify_AI
```

---

### Step 2: Install Dependencies

```bash
npm install
```

If npm gives a registry or timeout error, delete the old lock/install files and reinstall:

```bash
rm -rf node_modules package-lock.json
npm cache clean --force
npm install --registry=https://registry.npmjs.org/
```

For Windows PowerShell:

```powershell
Remove-Item -Recurse -Force node_modules -ErrorAction SilentlyContinue
Remove-Item -Force package-lock.json -ErrorAction SilentlyContinue
npm cache clean --force
npm install --registry=https://registry.npmjs.org/
```

---

### Step 3: Run Development Server

```bash
npm run dev
```

Open the URL shown in the terminal, usually:

```txt
http://localhost:5173
```

---

### Step 4: Build the Project

```bash
npm run build
```

A successful build creates a `dist/` folder.

---

### Step 5: Preview Production Build

```bash
npm run preview
```

Open the preview URL shown in the terminal.

---

## Deployment on Vercel

### Method 1: Deploy from GitHub

1. Push this project to GitHub.
2. Go to Vercel.
3. Click **Add New Project**.
4. Import the GitHub repository.
5. Use these settings:

```txt
Framework Preset: Vite
Build Command: npm run build
Output Directory: dist
Install Command: npm install
```

6. Click **Deploy**.
7. Copy and submit the final Vercel URL.

---

## Recommended GitHub Repository Settings

After pushing the project, add these details in GitHub repo settings:

### Description

```txt
Spotify-inspired GenAI music discovery prototype with prompt-to-session creation, Group Jam Agent, and trust controls.
```

### Topics

```txt
react
vite
vercel
genai
spotify
music-recommendation
product-prototype
frontend
```

---

## Product Flow

```txt
User prompt
    ↓
Mood and intent interpretation
    ↓
AI-generated listening session
    ↓
Song queue + explanation
    ↓
User feedback / trust control
    ↓
Improved future session simulation
```

---

## Why This Project Is Defensible

This prototype is strong because it is not trying to build a fake full-stack product with weak backend logic. Instead, it focuses on the part that matters for a product submission:

- clear user problem
- believable GenAI feature
- clean interactive UI
- deployable frontend
- privacy and trust thinking
- simple demo that judges can understand quickly

The project is intentionally scoped as a prototype, not a production Spotify clone.

---

## Current Limitations

This project is a frontend prototype, so it has some deliberate limitations:

- no real Spotify login
- no real Spotify Web API integration
- no real LLM API calls
- no database
- no user authentication
- no persistent memory across sessions

These limitations are acceptable for a prototype, but they should be clearly stated during submission or presentation.

---

## Future Improvements

- Add real Spotify Web API integration.
- Add OpenAI / Gemini / Claude API for real prompt-to-playlist generation.
- Add user authentication.
- Store session history and feedback.
- Add real collaborative listening logic.
- Add accessibility testing.
- Add analytics dashboard for user engagement.

---

## Demo Script

Use this flow while presenting:

1. Open the deployed Vercel link.
2. Explain the problem: users want music for situations, not just genres.
3. Enter a natural language prompt.
4. Show the generated session.
5. Explain the AI reasoning section.
6. Open the Group Jam feature.
7. Show trust/privacy controls.
8. End with future scope: real Spotify API + real LLM integration.

---

## Important Note

This project is an academic/product prototype inspired by Spotify-style user experience. It is not affiliated with Spotify and does not claim to use Spotify's proprietary recommendation system.

---

## Author

**Satyam Singh**  
GitHub: [satyam9140](https://github.com/satyam9140)

---

## Repository Link

[https://github.com/satyam9140/Spotify_AI](https://github.com/satyam9140/Spotify_AI)
