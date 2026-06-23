# 🤖 AgenticAI-Studio

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://python.org)
[![React Version](https://img.shields.io/badge/react-18.2.0-blue.svg)](https://reactjs.org)
[![FastAPI Version](https://img.shields.io/badge/fastapi-0.104.1-green.svg)](https://fastapi.tiangolo.com)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

> **Intelligent Autonomous Agents for Modern Workflows**

---

## 📖 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Frontend Guide](#frontend-guide)
- [Database Schema](#database-schema)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

**AgenticAI-Studio** is a powerful platform that enables you to create, manage, and deploy autonomous AI agents. These agents can independently plan tasks, use tools, adapt to changes, and operate with minimal supervision.

### Why AgenticAI-Studio?

- 🚀 **Boost Productivity**: Automate complex workflows
- 🧠 **Smart Decisions**: AI-powered decision making
- 🔧 **Flexible**: Customizable agent behaviors
- 🌐 **Connected**: Integrate with any API or tool
- 📈 **Scalable**: Handle multiple agents simultaneously

---

## ✨ Key Features

### 🤖 Autonomous Agents
- Create agents with custom personalities
- Set autonomy levels (Low/Medium/High)
- Define agent capabilities and tools
- Monitor agent performance in real-time

### 📋 Task Planning
- Multi-step task decomposition
- Automated task prioritization
- Dynamic task re-planning
- Progress tracking and reporting

### 🛠️ Tool Integration
- Web search capabilities
- File processing (PDF, Excel, Images)
- API integration (REST, GraphQL)
- Database operations
- Email automation
- Custom tool development

### 💬 Intelligent Chat
- Natural language interaction
- Context-aware conversations
- Command execution
- Task creation via chat
- Live status updates

### 📊 Dashboard & Analytics
- Real-time agent metrics
- Task completion statistics
- Performance visualizations
- System health monitoring
- Custom reports

---

## 🏗️ Architecture


---

## 🛠️ Tech Stack

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| Python | 3.10+ | Programming Language |
| FastAPI | 0.104.1 | Web Framework |
| SQLAlchemy | 2.0.23 | ORM |
| Alembic | 1.12.1 | Database Migrations |
| Pydantic | 2.5.0 | Data Validation |
| Google Gemini | 0.3.2 | AI Integration |
| Celery | 5.3.4 | Task Queue |
| Redis | 5.0.1 | Cache & Queue |
| WebSocket | 12.0 | Real-time Communication |
| JWT | 1.3.1 | Authentication |

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| React | 18.2.0 | UI Framework |
| Vite | 5.0.4 | Build Tool |
| Tailwind CSS | 3.3.6 | Styling |
| Material-UI | 5.14.18 | Component Library |
| React Router | 6.20.0 | Routing |
| Axios | 1.6.2 | HTTP Client |
| React Query | 3.39.3 | State Management |
| Recharts | 2.10.3 | Charts & Graphs |
| Framer Motion | 10.16.5 | Animations |

### Database
| Technology | Purpose | Environment |
|------------|---------|-------------|
| SQLite | Development Database | Dev/Test |
| PostgreSQL | Production Database | Production |

### DevOps
| Technology | Purpose |
|------------|---------|
| Docker | Containerization |
| Docker Compose | Multi-container Orchestration |
| Nginx | Reverse Proxy |
| GitHub Actions | CI/CD |

---

## 🚀 Quick Start

### Prerequisites

- Python 3.10 or higher
- Node.js 18.0 or higher
- npm or yarn package manager
- Git
- Gemini API Key ([Get it here](https://makersuite.google.com/app/apikey))

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/AgenticAI-Studio.git
cd AgenticAI-Studio

# Create virtual environment
python -m venv venv

# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
cd backend
pip install -r requirements.txt

# Setup environment variables
cp .env.example .env
# Edit .env and add your Gemini API key

# Initialize database
python init_db.py

# Run migrations
alembic upgrade head

# Start backend server
uvicorn app.main:app --reload --host 0.0.0.0 --port 5000

# Open new terminal
cd frontend

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env

# Start development server
npm run dev