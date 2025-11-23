# 🚨 Real-Time AI Command Center for Emergency Dispatch  
### **AI Triage • Intelligent Resource Allocation • Routing • Simulation**

This project implements a fully integrated **AI-powered Emergency Dispatch Command Center** designed to optimize triage, resource allocation, and routing in real-time. It combines **AI text classification**, **constraint-based recommendations**, **live fleet tracking**, and **simulation workflows** to support emergency response operations.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [System Architecture](#system-architecture)
- [Tech Stack](#tech-stack)
- [Folder Structure](#folder-structure)
- [Installation & Setup](#installation--setup)
- [Environment Variables](#environment-variables)
- [Running the Application](#running-the-application)
- [AI Subsystem](#ai-subsystem)
- [Routing & Mapping](#routing--mapping)
- [Simulation & Testing](#simulation--testing)
- [Screenshots](#screenshots)
- [Contributors](#contributors)

---

## 🧠 Overview
This system modernizes emergency medical dispatch workflows by providing:

- Automated **AI triage** of caller reports  
- Intelligent **resource and hospital recommendation**  
- Real-time **fleet tracking and routing**  
- End-to-end **incident simulation and auto-debriefs**

The system is validated using both standard and mass-casualty scenarios.

---

## ⭐ Key Features

### 🔹 AI Intelligence
- LLM-based incident triage (few-shot prompting)
- Key entity extraction from caller text
- Dispatch package recommendation
- Hospital recommendation using multi-constraint evaluation
- AI-generated protocols and traffic reports
- Automated incident debriefs

### 🔹 Command Center Capabilities
- Interactive dashboard for live incidents
- Responder fleet tracking on MapLibre
- Route visualization via OSRM
- Logging and incident timeline view
- Manual override controls

### 🔹 Simulation Tools
- 100+ scenario library (standard + disaster)
- Performance metrics:
  - Triage Accuracy
  - Recommendation Appropriateness
  - Simulated Response Time
- Automatic performance reporting

---

## 🏗️ System Architecture

### High-Level Workflow
1. Caller report received  
2. AI triage + key factors extraction  
3. Dispatch package recommendation  
4. Hospital suggestion  
5. OSRM route computation  
6. Command Center dashboard visualization  
7. AI-generated incident debrief  

### Major Components
- **AI Subsystem** (`src/ai/flows/*`)
- **Dashboard** (`src/components/dashboard/*`)
- **Incident Manager** (`src/components/incident/*`)
- **Routing & Maps** (`src/components/map/*`)
- **UI System** (ShadCN + Tailwind)

---

## 🧰 Tech Stack

### Frontend
- Next.js 14  
- React 18  
- TypeScript  
- Tailwind CSS + ShadCN UI  

### AI / NLP
- Google Genkit  
- LLM (Gemini/GPT)  
- BERT-based classifier (training analysis)

### Mapping & Routing
- MapLibre GL  
- React Map GL  
- OSRM (Open Source Routing Machine)

### Utilities
- geolib (Haversine distance)  
- Zustand / Context  
- Axios / Fetch  

---

## 📁 Folder Structure

src/
├── ai/
│ ├── flows/
│ │ ├── analyze-report.ts
│ │ ├── get-dispatch-package.ts
│ │ ├── recommend-hospital.ts
│ │ ├── get-protocol.ts
│ │ ├── get-traffic-report.ts
│ │ ├── summarize-incident.ts
│ │ └── debrief-incident.ts
│ └── genkit.ts
├── components/
│ ├── dashboard/
│ ├── incident/
│ ├── map/
│ └── ui/
├── theme/
├── utils/
└── pages/

yaml
Copy code

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/<your-org>/emergency-command-center.git
cd emergency-command-center
2. Install Dependencies
bash
Copy code
npm install
🔐 Environment Variables
Create a .env.local file:

env
Copy code
GOOGLE_GENKIT_API_KEY=your_key
OSRM_SERVER_URL=http://localhost:5000
NEXT_PUBLIC_MAPTILER_KEY=your_key
AI_MODEL=gemini-pro
🚀 Running the Application
Development
bash
Copy code
npm run dev
Visit: http://localhost:3000

Production
bash
Copy code
npm run build
npm start
🤖 AI Subsystem
1. Triage Classification
LLM-based few-shot prompting

Extracts key factors

Outputs confidence score

2. Dispatch Package Recommender
Determines vehicle types & counts

Supports multi-agency incidents

3. Hospital Recommendation
Evaluates:

Bed availability

Speciality match

Travel distance

Live traffic

4. Debrief Generator
Auto-generates timeline

Highlights failures & improvements

🗺️ Routing & Mapping
Map rendering with MapLibre

OSRM-based driving route computation

Multi-unit routing overlays

Real-time updates during dispatch

🧪 Simulation & Testing
Scenario Library
50 standard emergency cases

50 mass-casualty disaster cases

Metrics Evaluated
Triage accuracy

Recommendation correctness

Response time projections

Model Performance
Precision: 0.98–1.00

Recall: 0.96–1.00

F1-Score: High across all classes

Stable learning curve (no overfitting)

🖼 Screenshots
Screenshots should be placed under /public/screenshots.

Recommended screenshots:

Architecture Diagram

Command Center Dashboard

AI Triage Panel

Dispatch Confirmation

Route View

Incident Debrief

Classification Report

Learning Curve

👨‍💻 Contributors
Faizan Ahmed — CSE, Presidency University

Zoya Alam — CSE, Presidency University

Pavitra Hiremath — CSE, Presidency University
