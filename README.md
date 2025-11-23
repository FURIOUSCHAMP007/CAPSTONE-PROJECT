
# 🚨 Real-Time AI Command Center for Emergency Dispatch

### **AI Triage • Intelligent Resource Allocation • Routing • Simulation**

This repository contains a fully integrated **AI-powered Emergency Dispatch Command Center**, built to modernize emergency response through intelligent triage, advanced decision-making, real-time routing, and automated post-incident analysis.
It is designed for real-world emergency environments such as **ambulance dispatch centers**, **smart cities**, and **disaster response units**.

---

## 📌 Table of Contents

* [Overview](#overview)
* [Key Features](#key-features)
* [System Architecture](#system-architecture)
* [Tech Stack](#tech-stack)
* [Folder Structure](#folder-structure)
* [Installation & Setup](#installation--setup)
* [Environment Variables](#environment-variables)
* [Running the Application](#running-the-application)
* [AI Subsystem](#ai-subsystem)
* [Routing & Mapping](#routing--mapping)
* [Simulation & Testing](#simulation--testing)
* [Screenshots](#screenshots)
* [Contributors](#contributors)
* [License](#license)

---

## 🧠 Overview

Emergency dispatch systems in large urban environments often suffer from slow manual workflows, incorrect triage, and inefficient routing.
This platform solves those problems by combining:

* **Multimodal AI triage**
* **Intelligent dispatch recommendations**
* **Hospital selection based on capabilities, distance & traffic**
* **Real-time responder routing & fleet monitoring**
* **Complete simulation environment with performance analytics**
* **Auto-generated debrief reports for incident analysis**

The full methodology, architecture, algorithms, and experiments are documented in the research PDF.

---

## ⭐ Key Features

### 🔹 AI Intelligence

* NLP-based triage classification (LLM / BERT)
* Extraction of key incident factors
* Intelligent multi-agency vehicle recommendation
* Hospital ranking system with traffic & capability scoring
* AI-generated protocols, summaries, and debrief reports

### 🔹 Command Center Capabilities

* Real-time MapLibre-based dashboard
* Live fleet tracking with status indicators
* Incident creation, editing, and audit logs
* Dynamic routing via OSRM
* Manual overrides for critical situations

### 🔹 Simulation Tools

* Supports **100 simulation scenarios** (50 standard + 50 disaster)
* Visual evaluation workflow
* Performance metrics:

  * Triage Accuracy
  * Recommendation Appropriateness
  * Simulated Response Time

---

## 🏗️ System Architecture

### **High-Level Flow**

```
Caller Report → AI Triage → Dispatch Recommendations → Hospital Selection 
               → Route Computation (OSRM) → Command Center Dashboard 
               → Incident Debrief Generation
```

### **Major Components**

* **AI Subsystem**

  * Triage classifier
  * Dispatch package recommender
  * Hospital recommender
  * Protocol & traffic generator
  * Debrief generator

* **Dashboard System**

  * Analytics dashboard
  * Dispatch dashboard
  * Incident timeline & summaries
  * Fleet status monitor

* **Map & Routing**

  * MapLibre GL
  * React Map GL
  * OSRM (fast routing engine)

---

## 🧰 Tech Stack

### Frontend & UI

* Next.js 14
* React 18
* TypeScript
* Tailwind CSS
* ShadCN UI Components

### AI / ML

* Google **Genkit** (LLM Pipelines)
* BERT-based classifier (architecture referenced in analysis)
* Few-shot prompt engineering

### Maps & Routing

* MapLibre GL
* React Map GL
* **OSRM (Open Source Routing Machine)**
* Haversine-based nearest responder algorithm

### Utilities

* geolib
* Axios / Fetch
* Zustand or React Context

---

## 📁 Folder Structure

```
src/
 ├── ai/
 │    ├── flows/
 │    │    ├── analyze-report.ts
 │    │    ├── get-dispatch-package.ts
 │    │    ├── recommend-hospital.ts
 │    │    ├── get-protocol.ts
 │    │    ├── get-traffic-report.ts
 │    │    ├── summarize-incident.ts
 │    │    └── debrief-incident.ts
 │    └── genkit.ts
 ├── components/
 │    ├── dashboard/
 │    ├── incident/
 │    ├── map/
 │    └── ui/
 ├── theme/
 ├── utils/
 └── pages/
```

---

## ⚙️ Installation & Setup

### **1. Clone the Repository**

```bash
git clone https://github.com/<your-org>/ai-command-center.git
cd ai-command-center
```

### **2. Install Dependencies**

```bash
npm install
```

---

## 🔐 Environment Variables

Create a `.env.local` file:

```env
GOOGLE_GENKIT_API_KEY=your_key
OSRM_SERVER_URL=http://localhost:5000
NEXT_PUBLIC_MAPTILER_KEY=your_map_key
AI_MODEL=gemini-pro
```

---

## 🚀 Running the Application

### **Development Mode**

```bash
npm run dev
```

Access at:
👉 [http://localhost:3000](http://localhost:3000)

### **Production Build**

```bash
npm run build
npm start
```

---

## 🤖 AI Subsystem

### 1. **AI Triage Classification**

* Uses Few-Shot LLM (Genkit)
* Extracts key incident entities
* Outputs classification with confidence

### 2. **Dispatch Package Generator**

* Determines:

  * Ambulances
  * Fire units
  * Police units
  * Disaster response units

### 3. **Hospital Recommender**

Evaluates:

* Specialization match
* Bed availability
* Distance
* Traffic conditions

### 4. **Debrief Generator**

Creates:

* Timeline of events
* Key factors affecting outcome
* What went well
* Areas for improvement

---

## 🗺️ Routing & Mapping

### **Map Features**

* Live responder locations
* New incident markers
* Real-time view of fleet status

### **Routing Engine**

* OSRM via API
* Contraction Hierarchies routing
* Displays fastest driving route
* Supports multi-unit deployment

### **Nearest Responder Algorithm**

* Haversine formula (via geolib)
* Selects closest available responder

---

## 🧪 Simulation & Testing

### **Scenario Sets**

* **50 Standard Emergency Events**
* **50 Mass-Casualty / Disaster Events**

### **Evaluation Metrics**

* Triage Accuracy
* Recommendation Appropriateness
* Simulated Response Time

### **Model Performance (from Research)**

* Precision: **0.98–1.00**
* Recall: **0.96–1.00**
* F1 Score: **High across all categories**
* Stable learning curves (no overfitting)

---

## 🖼 Screenshots

*(Add these images inside `/public/screenshots/` in your repo)*

Suggested screenshots:

* System Architecture Diagram
* Command Center Dashboard
* AI Triage Panel
* Dispatch Confirmation Popup
* OSRM Route Visualization
* Incident Debrief Report
* Classification Report
* Learning Curve Plot

---

## 👨‍💻 Contributors

* **Faizan Ahmed** — Presidency University
* **Zoya Alam** — Presidency University
* **Pavitra Hiremath** — Presidency University

---

## 📜 License

MIT License (or select your preferred license)


