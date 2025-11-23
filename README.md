🚨 Real-Time AI Command Center for Emergency Dispatch
AI Triage • Intelligent Resource Allocation • Routing • Simulation • Command Center Dashboard

A fully integrated AI-driven emergency command center designed for real-time incident management, triage classification, resource allocation, hospital recommendation, routing, and simulation.
The system leverages Next.js, Google Genkit (LLM/AI), MapLibre + OSRM, and modular architecture for real-world deployment.

📌 Table of Contents

Overview

Key Features

System Architecture

Tech Stack

Folder Structure

Installation & Setup

Environment Variables

Running the Application

AI Subsystem

Routing & Mapping

Simulation & Testing

Screenshots / Figures

Contributors

🧠 Overview

This system addresses critical weaknesses in traditional emergency medical dispatch systems — such as slow manual triage, inefficient routing, and manual hospital selection — by integrating:

AI NLP triage classifier

AI-based dispatch package recommender

Hospital recommendation engine

Real-time map, routing, and fleet tracking

Simulated incident workflow with auto-generated debriefs

All of these are validated through 100+ simulated emergency scenarios (50 standard + 50 mass-casualty) 

A Real Time AI Command Center f…

.

⭐ Key Features
🔹 AI Features

Automatic triage of caller reports (LLM-based)

Entity extraction for key incident factors

Dispatch package recommendation

Intelligent hospital recommendation

AI-generated protocols & traffic analysis

Automated debrief report generation

🔹 Command Center Features

Live dashboard for active incidents

Real-time fleet tracking

Incident lifecycle management

Route visualization (fastest driving path)

Manual override for critical operations

🔹 Simulation Features

Scenario-based simulation (standard + disaster events)

Response-time evaluation

Classification accuracy reporting

AI failure-capture and debrief analysis

🏗️ System Architecture

The architecture consists of AI core + Dashboard + Routing + Simulation environment.

📌 High-Level Architecture (Page 1–2)

Caller → AI Triage → Recommended Dispatch → Hospital Recommendation → OSRM Routing → Command Center UI → Debrief


A Real Time AI Command Center f…

📌 Component Architecture (Page 2–3)

Modules include:

AI flows (src/ai/flows/*)

Dashboard (src/components/dashboard/*)

Incident management

MapLibre + OSRM routing layer

Reusable UI components


A Real Time AI Command Center f…

🧰 Tech Stack
Frontend / Command Center

Next.js 14

React 18

TypeScript

Tailwind CSS + ShadCN UI

React Map GL / MapLibre

AI / NLP / LLM

Google Genkit

LLM few-shot classification

BERT-based text model (training analysis)

Routing

OSRM (Open Source Routing Machine)

Contraction Hierarchies (fast routing)

Utilities

geolib (distance & Haversine)

Zustand / Context

Axios / Fetch

📁 Folder Structure
├── src/
│   ├── ai/
│   │   ├── flows/
│   │   │   ├── analyze-report.ts
│   │   │   ├── get-dispatch-package.ts
│   │   │   ├── recommend-hospital.ts
│   │   │   ├── get-protocol.ts
│   │   │   ├── get-traffic-report.ts
│   │   │   ├── summarize-incident.ts
│   │   │   └── debrief-incident.ts
│   │   └── genkit.ts
│   ├── components/
│   │   ├── dashboard/
│   │   ├── incident/
│   │   ├── map/
│   │   └── ui/
│   ├── theme/
│   ├── utils/
│   └── pages/
├── public/
├── package.json
└── README.md

⚙️ Installation & Setup
1. Clone the Repository
git clone https://github.com/<your-org>/emergency-command-center.git
cd emergency-command-center

2. Install Dependencies
npm install
# or
yarn install

3. Install OSRM (Required for routing)
Linux/Mac
brew install osrm-backend

Run OSRM with your map extract
osrm-extract map.osm.pbf -p profiles/car.lua
osrm-contract map.osrm
osrm-routed map.osrm


OR use a hosted OSRM server.

🔐 Environment Variables

Create a .env.local file:

GOOGLE_GENKIT_API_KEY=your_key
OSRM_SERVER_URL=http://localhost:5000
NEXT_PUBLIC_MAPTILER_KEY=your_key
AI_MODEL=gemini-pro   # or any supported Genkit model

🚀 Running the Application
Development Mode
npm run dev


Access at http://localhost:3000

Production Build
npm run build
npm start

🤖 AI Subsystem
🔹 Triage Classification

Uses Few-Shot LLM prompting

Extracts key entities

Produces incident type + confidence


A Real Time AI Command Center f…

🔹 Dispatch Package Generator

Recommends:

Number of ambulances

Fire units

Police units

Disaster response teams

🔹 Hospital Recommender

Evaluates:

Speciality match

Bed availability

Distance

Traffic

Live routing score


A Real Time AI Command Center f…

🗺️ Routing & Mapping

Map rendering using MapLibre/React-Map-GL

Routing calculated using OSRM with real-time paths

Route visualized as polyline

Supports multiple responder paths simultaneously


A Real Time AI Command Center f…

🧪 Simulation & Testing
✔ Standard Scenario Set — 50 incidents
✔ Disaster Scenario Set — 50 mass-casualty events
Evaluation Metrics (Fig. 5):

Triage Accuracy

Recommendation Appropriateness

Simulated Response Time


A Real Time AI Command Center f…

Model Metrics (Fig. 12):

Precision: 0.98–1.00

Recall: 0.96–1.00

F1-Score: Consistently high across all categories


A Real Time AI Command Center f…

Learning Curve (Fig. 13):

Stable convergence

No overfitting


A Real Time AI Command Center f…

🖼 Screenshots / Figures

Include visuals from the PDF:

Feature	Page
Architecture Diagram	Page 1–2
Command Center Dashboard	Page 4 (Fig. 6)
AI Triage Panel	Page 4 (Fig. 7)
Dispatch Confirmation	Page 4 (Fig. 8)
Routing Visualization	Page 5 (Fig. 9)
Debrief Panel	Page 5 (Fig. 11)
Classification Report	Page 5 (Fig. 12)
Learning Curve	Page 6 (Fig. 13)

Screenshots can be added inside /public/screenshots.

👨‍💻 Contributors

Faizan Ahmed, CSE, Presidency University

Zoya Alam, CSE, Presidency University

Pavitra Hiremath, CSE, Presidency University
