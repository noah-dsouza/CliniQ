# 🧠 ClinIQ

**AI-powered clinical trial matching + specialist sourcing**

> Turn patient data into actionable insights, personalized care, and real clinical trial opportunities.

🔗 **Devpost:** https://tinyurl.com/mv7mzvnt

---

## 🚀 Overview

ClinIQ creates a **digital twin** of a patient using real health data — then uses AI to match them with clinical trials, doctors, and personalized insights.

Instead of generic health tools, ClinIQ understands *your actual condition*.

---

## 🔍 What ClinIQ Does

### 🧬 Digital Twin Modeling

Builds a structured patient profile from:

* Labs, vitals, diagnoses
* Medications & comorbidities
* Lifestyle + uploaded medical documents

Automatically computes:

* ECOG Performance Status
* Charlson Comorbidity Index
* BMI + system-level health scores

---

### 🧪 Clinical Trial Matching

* Live data from **ClinicalTrials.gov**
* AI evaluates eligibility using real patient data
* Clear breakdown of:

  * Inclusion criteria ✅
  * Exclusion criteria ❌
* Plain-English explanations (no medical jargon overload)

---

### 🧑‍⚕️ Find Specialists

* **US:** NPI Registry (no API key required)
* **Global:** OpenStreetMap Overpass API
* Search by condition + location

---

### 💬 AI Health Assistant

* Powered by **Groq + Claude**
* Fully context-aware (knows patient data)
* Answers:

  * Lab results
  * Risk scores
  * Medications
  * Trial eligibility

---

### 🎮 Demo Mode

Skip onboarding and load a prebuilt patient:

* **58M**
* Type 2 Diabetes
* Hypertension
* Chronic Kidney Disease

---

## 🛠️ Tech Stack

| Layer         | Tech                                                 |
| ------------- | ---------------------------------------------------- |
| Frontend      | React, TypeScript, Vite, Framer Motion, Tailwind CSS |
| Backend       | Node.js, Express, TypeScript                         |
| AI            | Groq, Claude                                         |
| Trial Data    | ClinicalTrials.gov API + Web Scraping                |
| Doctor Search | NPI Registry (US) + OpenStreetMap Overpass API       |

---

## ⚙️ Getting Started

### 1. Install dependencies

```bash
npm run install:all
```

### 2. Set up environment variables

```bash
cp .env.example .env
```

Add your API key:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Get a free key at: https://console.groq.com

---

### 3. Run the app

```bash
# Terminal 1 — Backend (port 3001)
npm run dev:backend

# Terminal 2 — Frontend (port 5173)
npm run dev:frontend
```

Open: http://localhost:5173

---

## ✨ Features

### Digital Twin

* 6-step intake form OR document upload
* Structured health profile generation
* Automatic scoring + system-level analysis

---

### Clinical Trial Matching

* Real-time trial search
* AI eligibility scoring
* Detailed reasoning for each criterion

---

### Find Support

* Doctor search by specialty + location
* Works globally (no API key required)

---

### AI Chat

* Context-aware assistant
* Uses real patient data
* No generic answers

---

## 📁 Project Structure

```
cliniq/
├── frontend/          # React + Vite app
│   └── src/
│       ├── app/       # Components & pages
│       ├── context/   # DigitalTwinContext
│       ├── hooks/     # useIntakeForm
│       └── types/     # Shared types
├── backend/           # Express API
│   └── src/
│       ├── routes/    # chat, eligibility, trials, doctors, demo
│       ├── services/  # groqService, doctorSearchService, digitalTwinBuilder
│       └── types/     # Shared types
└── .env.example
```

---

## 💡 Why ClinIQ?

Most health tools give generic advice.

ClinIQ:

* Uses **your real data**
* Matches you to **actual clinical trials**
* Explains **why you qualify (or don’t)**
* Connects you with **real doctors**

Basically: less guessing, more precision.

---

## ⚠️ Disclaimer

ClinIQ is for **educational and research purposes only**.
Not intended for medical diagnosis or treatment decisions.
