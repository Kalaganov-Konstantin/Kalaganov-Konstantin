<div align="center">

🇺🇸 **English** | [🇷🇺 **Русский**](./README.md)

</div>

# Hi there! 👋 I'm Konstantin Kalaganov

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&pause=1000&color=36BCF7&center=true&vCenter=true&width=520&lines=Backend%20Developer;Python%20%26%20Go;Microservices%20%26%20Event-Driven%20Architecture;Fintech%2C%20Payments%2C%20IoT)](https://github.com/Kalaganov-Konstantin)

</div>

## 🚀 About Me

**Backend Developer** with ~3 years of production experience. Core stack — **Python** (FastAPI, async SQLAlchemy, Redis), with hands-on experience in **Go**.

I design and ship microservices from scratch for **fintech and IoT**: distributed payments with idempotency and fault tolerance, remote device fleet management, and migrating a monolith to event-driven architecture over Kafka. I focus on data reliability — Transactional Outbox, circuit breaker, deduplication — and on reusable internal libraries.

### 🎯 What I'm doing now

- 🔭 Backend Developer at **ATOL** — cloud platform for managing a fleet of fiscal devices
- ⚙️ Distributed systems, fault tolerance, and observability
- 🐹 Growing my expertise in **Go** and **Kubernetes**
- 👥 Regular code reviews and mentoring juniors

## 🛠️ Tech Stack

<div align="center">

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)

**Frameworks & Libraries**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/DRF-A30000?style=for-the-badge&logo=django&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white)

**Messaging & APIs**

![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=for-the-badge&logo=mqtt&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?style=for-the-badge&logo=google&logoColor=white)
![REST](https://img.shields.io/badge/REST%20API-005571?style=for-the-badge&logo=fastapi&logoColor=white)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=for-the-badge&logo=clickhouse&logoColor=black)
![Redis](https://img.shields.io/badge/Redis%20%2F%20Valkey-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)

**DevOps & Cloud**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI%2FCD-FC6D26?style=for-the-badge&logo=gitlab&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Jaeger](https://img.shields.io/badge/Jaeger-60A8C9?style=for-the-badge&logo=jaeger&logoColor=white)
![Sentry](https://img.shields.io/badge/Sentry-362D59?style=for-the-badge&logo=sentry&logoColor=white)
![ELK](https://img.shields.io/badge/ELK%20Stack-005571?style=for-the-badge&logo=elasticsearch&logoColor=white)

</div>

## 📈 By the Numbers

<div align="center">

**500K+** events/day via Kafka • **50K+** IoT devices • **5** payment providers

**5+** services on a shared library • **~12** services moved to non-root • **50+** code reviews • **3** juniors grown to middle

</div>

## 💼 Experience

### 🏢 ATOL — Backend Developer
`Dec 2025 — Present` · *Cloud microservice platform for managing a fleet of fiscal devices*

- Designed and shipped from scratch, as the lead developer, a **remote device access** microservice over **VNC**: connection lifecycle, MQTT-driven session start/stop, auto-cleanup of stuck sessions on timeout, auto-recovery on disconnect, protocol versioning; session state kept in Redis.
- Built a reusable internal **MQTT client library** with a publish queue, idempotent initialization, and structured logging; set up CI with auto-publishing to PyPI — adopted by **5+ services**.
- Implemented the **Transactional Outbox** pattern for guaranteed event delivery and extracted outbox + relay into a shared library.
- Implemented **bulk device operations**: group updates and config imports with aggregated status, filtering, and sorting.

<sub>**Stack:** Python 3.11+, FastAPI, SQLAlchemy 2.0 (async), Alembic, Pydantic v2, MQTT (aiomqtt / EMQX), Redis, Docker, GitLab CI/CD, Prometheus, Sentry</sub>

### 💳 B2B Fintech Platform — Backend Developer
`Dec 2025 — May 2026` · *Multi-tenant platform: payments, bonuses, cashback, reports, seamless wallet*

- Designed a **cascading payment orchestrator** with provider routing: on failure, the request automatically falls through to the next provider.
- Implemented payment **idempotency**: signature-based deduplication with a time window, per-record TTL with background cleanup, and state persistence for safe retries.
- Added a **circuit breaker** on Valkey to isolate failing providers.
- Integrated **5 payment providers**, including a seamless wallet: DB-level locking for idempotency, webhook verification, multi-tenancy, and timezone-aware daily withdrawal limits.
- Built a cashback system, eliminating data races with `SELECT FOR UPDATE`, plus v2 of the reporting API.

<sub>**Stack:** Python, FastAPI, Flask (legacy), SQLAlchemy 2.0, Alembic, Pydantic v2, Valkey/Redis, AWS (ECS, CloudFormation), boto3</sub>

### 🏠 Ufanet — Backend Developer
`Mar 2024 — Dec 2025` · *"Smart Intercom" ecosystem of dozens of microservices*

- Designed and led the migration of a distributed monolith to an **event-driven architecture**: moved synchronous HTTP calls to async processing over Kafka, handling **500K+ events/day** with batching and partitioning.
- Built, as a core contributor, a **utility (ЖКХ) billing service**: invoicing and tariffs tied to buildings/entrances/apartments, acquiring, Kafka sync, reminders and push via Celery, analytics in ClickHouse.
- Maintained an **access-key service for 50K+ devices**: key activation and replacement, BLE, webhooks on device discovery, real-time state monitoring over MQTT.
- Implemented an **anti-corruption layer** between the legacy and new intercom services with two-way contract sync — enabling a gradual, zero-downtime migration.
- Wrote intercom services in **Go** over MQTT: device subscriptions with recovery and a mutex-based concurrency model, call integration, and SIP-monitor support.
- Set up CI/CD, Prometheus/Grafana monitoring, and Jaeger tracing. Ran **50+ code reviews** and mentored **3 juniors** to middle level.

<sub>**Stack:** Python, Go, Django, DRF, FastAPI, SQLAlchemy 2.0 (async), Celery, Kafka, MQTT, gRPC, PostgreSQL, ClickHouse, Redis, Docker, Kubernetes, Prometheus, Grafana, Jaeger</sub>

### 🤖 Crypton (startup) — Python Developer
`Mar 2023 — Mar 2024` · *Cryptocurrency monitoring service*

- Built a **Telegram bot** on aiogram: alerts on price thresholds and technical indicators (RSI, MACD).
- Integrated the **Binance** and **CoinGecko** APIs for real-time data, optimized external requests, and added Redis caching.
- Built a **REST API** on FastAPI and PostgreSQL for the web version; automated deployment and DB backups with bash scripts.

<sub>**Stack:** Python, aiogram, FastAPI, TA-Lib, PostgreSQL, Redis</sub>

## 🎓 Education

**Ufa State Aviation Technical University**, 2022 — Heat Power Engineering (Automated Control Systems track).

## 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Kalaganov-Konstantin&theme=github_dark&hide_border=false&include_all_commits=true&count_private=true" height="160" alt="GitHub Stats" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kalaganov-Konstantin&theme=github_dark&hide_border=false&layout=compact&langs_count=8" height="160" alt="Top Languages" />

</div>

## 🤝 Let's Connect

<div align="center">

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kalaganov.konstant@gmail.com)
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/KalaganovKonstantin)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Kalaganov-Konstantin)

📍 **Ufa, Russia** · 🌐 **Open to remote work and relocation** · 🗣️ **Russian (native), English B2**

![Profile Views](https://komarev.com/ghpvc/?username=Kalaganov-Konstantin&color=blueviolet&style=flat-square)

</div>