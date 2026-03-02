# 🧠 DiverEdu

**AI-powered educational platform that adapts content for neurodivergent students — supporting dyslexia, ADHD, and dyscalculia.**

> 🏆 **1st Place** — [Hack4EDU 2024](https://hack4edu.es/) by ProFuturo (Telefónica)

![Vue.js](https://img.shields.io/badge/Vue.js-3-4FC08D?logo=vuedotjs&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-API-000000?logo=flask)
![GPT-4o](https://img.shields.io/badge/OpenAI-GPT--4o-412991?logo=openai&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker&logoColor=white)

## What is DiverEdu?

DiverEdu gives teachers a dashboard to generate adapted lessons using AI. Each lesson is produced in three formats tailored to different learning needs:

- **Bionic Reading** — Bolds the first syllables of each word (via `pylabeador` for Spanish segmentation), helping students with ADHD maintain reading focus.
- **Emoji Word Replacement** — Substitutes key words with emoji cues, providing visual anchors for students with dyslexia.
- **Standard Format** — Clean, structured content for neurotypical students.

Additional features:

- **Empathy Quiz Exercises** — Simulates the experience of dyscalculia for neurotypical students, building classroom empathy.
- **AI Course Generation** — Teachers describe a topic and GPT-4o generates full lesson content in all three formats automatically.
- **Teacher Dashboard** — Create, manage, and preview adapted lessons from a single interface.

## Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Frontend** | Vue.js 3, Vuetify, Pinia, Tailwind CSS, Chart.js |
| **Backend** | Python, Flask, Flask-RESTX, pylabeador |
| **AI** | OpenAI GPT-4o |
| **Infrastructure** | Docker, Docker Compose, Nginx |

## Getting Started

### Prerequisites

- Docker & Docker Compose
- An [OpenAI API key](https://platform.openai.com/api-keys)

### Run

```bash
# Clone the repo
git clone https://github.com/mariops03/Hack4Edu2024-DiverEdu.git
cd Hack4Edu2024-DiverEdu

# Set your API key
export OPENAI_API_KEY=your-key-here

# Launch both services
docker-compose up --build
```

The frontend will be available through Nginx and the Flask API will be running behind it.

## Architecture

```
DiverEdu/
├── client/          # Vue.js 3 frontend (Vuetify + Tailwind)
├── server/          # Flask REST API (GPT-4o integration)
├── docker-compose.yml
└── nginx/           # Reverse proxy config
```

## Team

| Name | GitHub |
|------|--------|
| Daniel Mulas | [@danimulas](https://github.com/danimulas) |
| Mario Prieta | [@mariops03](https://github.com/mariops03) |
| Tomas Perez | [@Tomypv](https://github.com/Tomypv) |
| David Sanchez | [@DavidSanSan110](https://github.com/DavidSanSan110) |
