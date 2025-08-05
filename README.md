# Fitness_Buddy

# Fitness Buddy 🤖🏋️‍♀️

**Fitness Buddy** is an AI-powered virtual fitness coach that designs personalized home workouts, suggests nutritious meal plans, delivers motivational nudges, and tracks your progress—24/7, on any device.

---

## Table of Contents

1. [Features](#features)  
2. [Tech Stack](#tech-stack)  
3. [Architecture](#architecture)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
   - [Configuration](#configuration)  
5. [Usage](#usage)  
6. [Deployment](#deployment)  
7. [Contributing](#contributing)  
8. [License](#license)  

---

## Features

| Category             | Capabilities                                                                 |
|----------------------|-------------------------------------------------------------------------------|
| Workout Generator    | – Custom routines by duration, equipment & goal                                |
| Meal Planner         | – High-protein, vegetarian, keto, or macro-balanced recipes                    |
| Motivational Nudges  | – Daily tips to reinforce habits                                              |
| Progress Tracking    | – Habit streaks, workouts completed, calories logged                           |
| Analytics Dashboard  | – Charts on adherence, user satisfaction                                       |
| Personalization      | – Real-time adjustments based on user feedback                                 |
| Zero-Cost Entry      | – IBM Cloud Lite tier & open-source models                                     |

---

## Tech Stack

- **AI & NLP**  
  - IBM watsonx.ai Studio (Prompt Lab)  
  - IBM watsonx.ai Runtime  
  - IBM Agent Lab  
  - IBM Granity Foundation Model (RAG)  

- **Backend & Logic**  
  - Node.js + Express  
  - IBM Cloud Functions  

- **Data Storage**  
  - IBM Cloudant or Cloud SQL  

- **Frontend (Optional)**  
  - React / Next.js on IBM Code Engine  

- **DevOps & CI/CD**  
  - GitHub Actions  
  - IBM Cloud CLI & Terraform  

---

## Architecture

```plaintext
┌─────────────┐       ┌──────────────────┐      ┌───────────────┐
│   Client    │──────▶│ API Gateway /    │─────▶│  IBM Cloud    │
│ (Web/Mobile)│       │ Express Server   │      │ watsonx.ai     │
└─────────────┘       └──────────────────┘      └───────────────┘
                              │
                              ▼
                       ┌─────────────┐
                       │ Cloudant /  │
                       │ Cloud SQL   │
                       └─────────────┘


PUBLIC ENDPOINT : https://eu-gb.ml.cloud.ibm.com/ml/v4/deployments/dde75389-383a-4560-ba89-bdec72686f38/ai_service?version=2021-05-01
