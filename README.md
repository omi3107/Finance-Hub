<p align="center">
  <h1 align="center">💰 Finance Hub — Your Financial Digital Twin</h1>
  <p align="center">
    <strong>A comprehensive personal finance & tax management platform</strong>
  </p>
  <p align="center">
    <em>Track income & expenses · Auto-categorize transactions · Budget with 50-30-20 · Estimate taxes · Monitor credit health · Simulate your financial future</em>
  </p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Next.js-16-000000?logo=next.js&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
</p>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [API Reference](#-api-reference)
- [AI Engine Services](#-ai-engine-services)
- [Data Models](#-data-models)
- [Demo Flow](#-demo-flow)
- [Disclaimer](#-disclaimer)
- [Team](#-team)

---

## 🌟 Overview

**FinMirror** is a full-stack personal finance intelligence platform built for the Indian context. It enables users to consolidate financial data from multiple sources (bank statements, wallets, cards), receive AI-powered insights, and simulate their financial future through a **Digital Financial Twin**.

All financial intelligence is powered by a **deterministic, rule-based engine** — every recommendation is explainable, transparent, and free of black-box ML models. The platform is designed to be privacy-first with no external data sharing.

---

## ✨ Key Features

### 💳 Transaction Management
- **Multi-source ingestion** — Bank CSV, Paytm wallet, card statements, and manual entry
- **AI-powered categorization** — Automatic merchant-to-category mapping with confidence scores
- **Recurring transaction detection** — Identifies subscriptions and repeating expenses

### 📊 Budget & Behavior Analysis
- **50-30-20 rule enforcement** — Needs / Wants / Savings classification with violation alerts
- **Spending pattern analysis** — Month-over-month trends, top categories, anomaly detection
- **Budget health scoring** — Quantified financial discipline metric

### 🏦 Credit Health Score
- **Simulated credit score** (300–900) — Based on payment regularity, credit utilization, and loan discipline
- **Explainable breakdown** — Per-factor scoring with improvement suggestions
- **Loan management** — EMI tracking, prepayment analysis, debt-to-income monitoring

### 🧾 Tax Estimation (India-Specific)
- **Old vs. New regime comparison** — FY 2024–25 tax slabs
- **Deduction optimization** — Section 80C, 80D, 80CCD(1B), HRA, and more
- **Tax-saving suggestions** — Actionable recommendations with quantified savings

### 🎯 Goal-Based Savings
- **Financial goal creation** — Emergency fund, car, vacation, education
- **Progress tracking** — Visual progress bars with projected completion dates
- **Monthly contribution planning** — Required savings rate calculations

### 🤖 Digital Financial Twin
- **Future simulation** — 12-month financial projections based on current behavior
- **Scenario analysis** — Baseline, increased savings, job loss, EMI prepayment
- **Net worth forecasting** — Tracks savings growth, debt reduction, and goal feasibility

### 🛡️ Emergency Shield
- **Emergency fund adequacy check** — 3-month expense coverage analysis
- **Financial safety scoring** — Holistic risk assessment

### 📈 Investment Intelligence
- **Investment readiness gate** — Evaluates if user is financially ready to invest
- **Risk profile classification** — Stability-Focused / Growth-Ready / Growth-Optimized
- **Agent explanation layer** — Natural language explanations for all recommendations
- **Live stock market data** — Real-time market information integration

### 🔔 Smart Alerts
- **Overspending warnings** — Triggered when budget buckets are exceeded
- **Tax deadline reminders** — ITR filing, advance tax dates
- **Goal progress alerts** — On-track / at-risk notifications

---

## 🏗 Architecture

```
┌──────────────────────────────────────────────────────┐
│              Frontend (Next.js 16 + React 19)        │
│         Tailwind CSS · shadcn/ui · Recharts          │
└─────────────────────┬────────────────────────────────┘
                      │ REST API (JSON)
                      ▼
┌──────────────────────────────────────────────────────┐
│         Backend API (Node.js + Express 5 + TS)       │
│        JWT Auth · Mongoose ODM · MongoDB             │
└─────────────────────┬────────────────────────────────┘
                      │ Internal HTTP/JSON
                      ▼
┌──────────────────────────────────────────────────────┐
│           AI Engine (Python + FastAPI)                │
│     Rules Engine · Digital Twin · Tax Logic           │
│         Stateless · Deterministic · Explainable      │
└──────────────────────────────────────────────────────┘
```

### Design Principles

| Principle | Implementation |
|-----------|---------------|
| **Stateless AI** | AI Engine receives full context per request, never accesses DB directly |
| **Explainable** | Every recommendation includes reasoning — no black-box predictions |
| **Privacy-first** | No external API data sharing, all processing is local |
| **Microservice** | AI Engine is independently deployable and testable |
| **Rule-based** | Deterministic financial logic — outcomes are reproducible |

---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose |
|-----------|---------|
| **Next.js 16** | React framework with App Router, SSR, and middleware |
| **React 19** | UI component library |
| **Tailwind CSS 4** | Utility-first styling |
| **shadcn/ui + Radix UI** | Accessible, headless component primitives |
| **Recharts** | Data visualization (pie charts, line charts, gauges) |
| **Zod** | Schema validation |
| **React Hook Form** | Form state management |
| **Lucide React** | Icon library |

### Backend
| Technology | Purpose |
|-----------|---------|
| **Node.js + Express 5** | REST API server |
| **TypeScript** | Type-safe backend development |
| **MongoDB + Mongoose** | Document database with ODM |
| **JWT (jsonwebtoken)** | Session-less authentication |
| **bcrypt** | Password hashing |
| **Axios** | HTTP client for AI Engine integration |

### AI Engine
| Technology | Purpose |
|-----------|---------|
| **Python 3.11+** | Runtime |
| **FastAPI** | High-performance async API framework |
| **Pydantic** | Data validation and serialization |
| **pdfplumber** | Bank statement PDF parsing |
| **pytest** | Testing framework |
| **uvicorn** | ASGI server |

---

## 📁 Project Structure

```
HackVengers/
├── frontend/                    # Next.js 16 Application
│   ├── app/                     # App Router pages
│   │   ├── auth/                # Login & Sign-up pages
│   │   └── dashboard/           # Protected dashboard pages
│   │       ├── accounts/        # Payment accounts management
│   │       ├── budget/          # Budget overview & 50-30-20
│   │       ├── categories/      # Transaction categories
│   │       ├── emergency-fund/  # Emergency fund tracking
│   │       ├── goals/           # Financial goals
│   │       ├── investments/     # Investment portfolio
│   │       ├── loans/           # Loan & EMI management
│   │       ├── recurrings/      # Recurring subscriptions
│   │       ├── tax/             # Tax estimation & ITR
│   │       ├── transactions/    # Transaction history
│   │       └── virtual-twin/    # Digital Financial Twin
│   ├── components/              # React components
│   │   ├── ui/                  # 57 shadcn/ui primitives
│   │   ├── dashboard/           # Dashboard widgets & charts
│   │   ├── investments/         # Investment UI components
│   │   ├── goals/               # Goal tracking components
│   │   └── tax/                 # Tax estimation components
│   ├── lib/                     # Utilities & API client
│   └── hooks/                   # Custom React hooks
│
├── backend/                     # Node.js + Express API
│   └── src/
│       ├── config/              # Environment & constants
│       ├── controllers/         # 20 route controllers
│       ├── models/              # 11 Mongoose schemas
│       ├── routes/              # 21 API route modules
│       ├── services/            # 20 business logic services
│       ├── middleware/           # Auth, error handling
│       ├── integrations/        # AI Engine HTTP client
│       ├── utils/               # Helpers & utilities
│       └── types/               # TypeScript type definitions
│
├── ai-engine/                   # Python FastAPI Microservice
│   ├── main.py                  # Application entry point
│   ├── requirements.txt         # Python dependencies
│   ├── app/
│   │   ├── routers/             # 12 API endpoint routers
│   │   ├── services/            # 12 business logic services
│   │   ├── rules/               # Deterministic rule definitions
│   │   ├── models/              # Pydantic schemas
│   │   ├── core/                # Config, logging, constants
│   │   └── utils/               # Date, currency, calculators
│   └── tests/                   # Pytest test suite
│
└── docs/                        # Project documentation
    └── api-contracts.md         # API contract definitions
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** ≥ 18.x
- **Python** ≥ 3.11
- **MongoDB** (local or [MongoDB Atlas](https://www.mongodb.com/atlas))
- **npm** (comes with Node.js)

### 1. Clone the Repository

```bash
git clone https://github.com/KalpeshEragi/HackVengers.git
cd HackVengers
```

### 2. Backend Setup

```bash
cd backend
npm install

# Create environment file
cp .env.example .env
# Edit .env with your MongoDB URI and JWT secret

# Start development server
npm run dev
```

The backend server will start on **http://localhost:5000**

### 3. AI Engine Setup

```bash
cd ai-engine

# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate
# Activate (macOS/Linux)
# source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start the AI engine
python main.py
```

The AI engine server will start on **http://localhost:8000** (with interactive docs at `/docs`)

### 4. Frontend Setup

```bash
cd frontend
npm install

# Start development server
npm run dev
```

The frontend will be available at **http://localhost:5137**

### 5. Seed Demo Data (Optional)

```bash
cd backend
npm run seed:demo
```

---

## 🔐 Environment Variables

### Backend (`backend/.env`)

| Variable | Description | Default |
|----------|-------------|---------|
| `PORT` | Backend server port | `5000` |
| `NODE_ENV` | Environment mode | `development` |
| `MONGODB_URI` | MongoDB connection string | `mongodb://localhost:27017/hackvengers` |
| `JWT_SECRET` | Secret key for JWT signing | — (required) |
| `JWT_EXPIRES_IN` | Token expiration duration | `7d` |
| `AI_ENGINE_URL` | URL of the Python AI Engine | `http://localhost:5000` |

> **Note:** Copy `backend/.env.example` to `backend/.env` and fill in your values. Never commit `.env` to version control.

---

## 📡 API Reference

### Backend API Routes

| Method | Route | Description |
|--------|-------|-------------|
| `POST` | `/auth/register` | User registration |
| `POST` | `/auth/login` | User login (returns JWT) |
| `GET` | `/auth/me` | Get current user profile |
| `GET/POST` | `/transactions` | Transaction CRUD & bulk import |
| `GET/POST` | `/budget` | Budget management |
| `GET` | `/credit` | Simulated credit health score |
| `GET/POST` | `/tax` | Tax estimation & deductions |
| `GET/POST` | `/goals` | Financial goal management |
| `GET` | `/dashboard` | Aggregated financial insights |
| `GET` | `/alerts` | User notifications & alerts |
| `POST` | `/categorization` | AI-powered transaction categorization |
| `GET/POST` | `/payment-methods` | Payment account management |
| `GET/POST` | `/recurrings` | Recurring transaction tracking |
| `GET/POST` | `/investments` | Investment portfolio management |
| `GET/POST` | `/loans` | Loan & EMI management |
| `GET` | `/ledger` | Aggregated financial ledger |
| `POST` | `/investment-agent` | Investment readiness assessment |
| `GET` | `/risk-profile` | Risk profile classification |
| `GET` | `/investment-recommendations` | Personalized investment suggestions |
| `GET` | `/agent` | Agent explanation layer |
| `GET` | `/stocks` | Live stock market data |
| `GET/POST` | `/emergency-shield` | Emergency fund assessment |
| `GET` | `/balance` | Ledger-correct balance accounting |

### AI Engine API Routes

| Method | Route | Description |
|--------|-------|-------------|
| `GET` | `/health` | Health check |
| `POST` | `/categorize` | Transaction categorization |
| `POST` | `/behavior/analyze` | Spending behavior analysis (50-30-20) |
| `POST` | `/credit/analyze` | Credit health scoring |
| `POST` | `/tax/estimate` | Tax estimation (Old vs. New regime) |
| `POST` | `/tax/suggestions` | Tax-saving suggestions |
| `POST` | `/goals/plan` | Goal feasibility & planning |
| `POST` | `/twin/simulate` | Digital Financial Twin simulation |
| `POST` | `/alerts/check` | Alert generation |
| `POST` | `/parse` | Bank statement parsing (CSV/PDF) |
| `POST` | `/budget` | Budget agent analysis |
| `POST` | `/investment/readiness` | Investment readiness gate |
| `POST` | `/agent/explanation` | Natural language explanations |

---

## 🧠 AI Engine Services

The AI Engine is a **stateless microservice** that performs all financial intelligence computations. It never accesses the database directly — all context is provided in the request payload.

| Service | Responsibility |
|---------|---------------|
| **Categorization Service** | Maps merchant names to spending categories with confidence scores |
| **Behavior Service** | Analyzes spending patterns, detects 50-30-20 violations, generates suggestions |
| **Credit Service** | Computes simulated credit health score (300–900) with explainable factors |
| **Tax Service** | India-specific tax estimation — FY 2024-25 slabs, 80C/80D deductions, regime comparison |
| **Goal Service** | Savings goal planning — required monthly contributions, projected completion |
| **Digital Twin Service** | 12-month financial projection engine with scenario simulation |
| **Alert Service** | Deadline reminders, overspending alerts, compliance checks |
| **Statement Parser Service** | Parses bank/wallet CSV and PDF statements into structured transactions |
| **Budget Agent Service** | Intelligent budget allocation and rebalancing recommendations |
| **Investment Readiness Service** | Gate that evaluates if user is financially ready to invest |
| **Agent Explanation Service** | Generates natural language explanations for all AI decisions |

---

## 📦 Data Models

The backend uses **MongoDB** with **Mongoose** ODM. Key data models:

| Model | Description |
|-------|-------------|
| `User` | Authentication, profile, and financial summary |
| `Transaction` | Individual financial transactions (multi-source) |
| `Budget` | Monthly budget allocations and limits |
| `Goal` | Savings goals with targets and deadlines |
| `Loan` | Active loans with EMI schedules |
| `Investment` | Investment holdings (MF, FD, stocks) |
| `CreditSnapshot` | Point-in-time credit health assessments |
| `TaxProfile` | Income sources, deductions, and tax computations |
| `Alert` | System-generated user notifications |
| `PaymentMethod` | Linked bank accounts, wallets, and cards |
| `Recurring` | Detected recurring transactions and subscriptions |

---

## 🎬 Demo Flow

1. **Register & Login** — Create account → JWT authentication
2. **Add Income** — Set monthly salary and other income sources
3. **Import Transactions** — Upload Paytm/bank CSV or add manually
4. **Auto-Categorization** — Transactions auto-classified into Needs/Wants/Savings
5. **Budget Insights** — View 50-30-20 analysis with violation alerts
6. **Financial Mirror** — See behavioral spending insights and trends
7. **Credit Health** — View simulated credit score with improvement tips
8. **Tax Estimation** — Compare Old vs. New regime, get deduction suggestions
9. **Digital Twin** — Simulate 12-month financial future
10. **Goal Planning** — Create savings goals, track progress

---

## ⚠️ Disclaimer

- All financial insights are **estimations** and should not be treated as professional financial advice
- Credit scores are **simulated** (not actual CIBIL scores)
- Tax calculations are **estimates** for FY 2024–25 salary income only
- No real bank APIs or live payment integrations are used
- This is a **hackathon MVP** — not production-ready financial software

---

## 👥 Team

**HackVengers** — Built during a fintech hackathon (PS-12: Comprehensive Personal Finance & Tax Management Platform)

---

## 📄 License

ISC

---

<p align="center">
  <sub>Built with ❤️ by <strong>HackVengers</strong></sub>
</p>

