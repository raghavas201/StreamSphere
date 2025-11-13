# 🎥 StreamSphere – Cloud-Based Video Streaming Platform

StreamSphere is a full-stack **video streaming application** inspired by YouTube — built using **AWS**, **FastAPI**, **Docker**, **Redis**, **PostgreSQL**, and **Flutter (Bloc)**.  
It demonstrates scalable backend architecture, cloud-based video delivery, and a responsive cross-platform frontend.

---

## 🚀 Features

- ⚡ **Scalable Cloud Backend** – Deployed on AWS using ECS and S3 for storage.
- 🧠 **Asynchronous FastAPI Server** – Handles uploads, streaming, and user management efficiently.
- 🧱 **Dockerized Microservices** – Simplifies deployment, portability, and version control.
- 🗃️ **Redis Caching** – Boosts performance and reduces API latency.
- 🐘 **PostgreSQL Database** – Robust data storage for user profiles, video metadata, and analytics.
- 📱 **Flutter + Bloc Frontend** – Modern, responsive UI for mobile and web clients.

---

## 🧩 Tech Stack

**Frontend:** Flutter, Dart, Bloc  
**Backend:** FastAPI, Python  
**Database:** PostgreSQL  
**Caching:** Redis  
**Cloud Infrastructure:** AWS (EC2, ECS, S3, RDS)  
**Containerization:** Docker  
**Version Control:** Git, GitHub  

---

## 🏗️ Architecture Overview

```text
                ┌─────────────────────────────┐
                │         Flutter App          │
                │ (Mobile & Web using Bloc)    │
                └──────────────┬───────────────┘
                               │ REST API Calls
                               ▼
                ┌─────────────────────────────┐
                │          FastAPI API         │
                │  Authentication, Uploads,    │
                │  Streaming, Video Metadata   │
                └──────────────┬───────────────┘
                     │                   │
         ┌───────────┘                   └─────────────┐
         ▼                                             ▼
┌────────────────────┐                      ┌─────────────────────┐
│    PostgreSQL DB    │                      │     Redis Cache     │
│ (User & Video Data) │                      │   (Session, Caching)│
└────────────────────┘                      └─────────────────────┘
                     ▼
          ┌────────────────────┐
          │       AWS S3        │
          │ (Video Storage CDN) │
          └────────────────────┘






