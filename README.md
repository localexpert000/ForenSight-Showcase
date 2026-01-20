# ForenSight AI: The Edge-First Surveillance Intelligence Platform

![ForenSight Banner](https://via.placeholder.com/1200x400?text=ForenSight+AI+Surveillance+System)

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
![React](https://img.shields.io/badge/React-19.2-61DAFB?style=for-the-badge&logo=react)
![YOLOv8](https://img.shields.io/badge/AI-YOLOv8-green?style=for-the-badge)
![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?style=for-the-badge&logo=fastapi)
![License](https://img.shields.io/badge/License-Academic%20Project-red?style=for-the-badge)

**Real-Time · Privacy-Focused · 100% Local Processing · Zero Monthly Cost**

</div>

---

## 📖 Executive Summary

**ForenSight AI** is a comprehensive software ecosystem designed to solve the critical flaws in modern CCTV surveillance: **Passive Recording**, **High Latency**, and **Prohibitive Cloud Costs**.

Built as a Final Year Project for the **Department of Information and Communication Engineering**, this system introduces a **Hybrid Edge-Cloud Architecture**. It processes video streams locally on commodity hardware (laptops) using advanced AI models, ensuring data ownership and millisecond-level responsiveness, while utilizing a serverless cloud relay for worldwide secure access.

### 🛑 The Problem
*   **Traditional NVRs** are "dumb" recording boxes that only provide evidence *after* a crime.
*   **Cloud Cameras (Ring/Nest)** destroy bandwidth and have localized privacy risks.
*   **Enterprise AI (Verkada)** costs thousands of dollars per camera annually.

### ✅ The ForenSight Solution
*   **Smart:** 59+ Verified Detection Features (Weapons, Fire, Faces, Behavior).
*   **Fast:** <100ms Inference Time via local Edge processing.
*   **Free:** Utilizes CloudFlare Tunnels and Local Storage for **$0/month** operation.

---

## 🚀 Key Features (Verified)

We have verified and implemented over 50 distinct AI modules across 4 categories:

| **Category** | **Key Capabilities** |
| :--- | :--- |
| **🕵️ Human Analytics** | Face Recognition (ArcFace), Person Re-ID, Crowd Counting, Uniform Detection. |
| **🛡️ Security** | **Weapon Detection** (Pistols/Rifles), **Fire/Smoke Detection**, Intrusion Zones, Fighting Detection. |
| **🚗 Vehicle Analytics** | **ALPR** (License Plate Rec), Vehicle Color/Type Classification, Wrong-Way Detection. |
| **🧠 Behavioral** | **Loitering Detection**, Panic/Running Analysis, Abandoned Object Detection. |

> *Full technical feature list available in [FEATURES.md](./FEATURES.md)*

---

## 🏗️ System Architecture

ForenSight utilizes a **Decentralized 4-Tier Architecture**:

1.  **Tier 1: Edge Node (Python/PyQt6)** - Runs on-site. Grabs RTSP feeds, runs YOLOv8/ArcFace inference, and stores encrypted logs locally.
2.  **Tier 2: Secure Tunnel (CloudFlare)** - Exposes the local API to the web via a secure, zero-trust outbound connection.
3.  **Tier 3: Central Relay (FastAPI/PostgreSQL)** - Handles User Authentication (OAuth2) and signals routing.
4.  **Tier 4: Client Portal (React 19)** - A modern SPA for viewing live feeds and alerts from anywhere in the world.

```mermaid
graph TD
    subgraph Edge [Local Edge Node (Your Laptop)]
        Cam[IP Cameras] -->|RTSP| App[Edge App]
        App -->|Inference| AI[YOLOv8 + InsightFace]
        App -->|Storage| DB[(SQLite)]
    end

    subgraph Internet [Secure Cloud Layer]
        Tunnel[CloudFlare Tunnel]
        Relay[Central API]
    end

    subgraph User [Remote Access]
        Web[React Dashboard]
        Admin[Admin Panel]
    end

    App -->|Encrypted HTTPS| Tunnel --> Relay
    Relay -->|Signals| Web
    Web -->|Live Stream| Tunnel
```

---

## 🛠️ Technology Stack

We use the latest verified stable versions (2025/2026 standard):

*   **Frontend:** React 19.2, Vite 7.2, TailwindCSS 3.4
*   **Backend:** FastAPI 0.115, Uvicorn, PostgreSQL 16
*   **AI/ML:** Ultralytics YOLO v8.3, OpenCV 4.12, InsightFace 0.7.3
*   **Security:** OAuth2 (JWT), Bcrypt, Fernet Encryption (Logs)
*   **DevOps:** CloudFlare Tunnels (Zero Trust)

---

## 📸 Project Verification

This repository acts as a **Portfolio Showcase**. The main codebase is strictly modularized:

*   `demo_pipeline.py`: A showcased architectural snippet demonstrating our clean-code practices for the ingestion pipeline.
*   **Report**: A full 30-page engineering report is available upon request.

---

## 👨‍💻 Developer & Acknowledgements

**Developed by:** Asad  
**Department:** Information and Communication Engineering  
**Specialization:** Cyber Security & Digital Forensics (4th Semester)

*Special thanks to my teachers and mentors for their guidance on ethical surveillance and forensic standards.*
