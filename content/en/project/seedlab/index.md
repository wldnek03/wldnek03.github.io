---
title: Seed Lab Digital Twin (Capstone Project)
summary: A real-time digital twin system for monitoring seed propagation environments. Implemented MQTT/WebSocket-based data processing, Linux server operations, Docker deployment, and an LLM chatbot powered by Groq API. Leveraged Claude Code to improve development productivity and automate operational tasks.
tags:
  - IoT
  - Backend
  - Capstone
  - Digital Twin
  - LLM
date: 2026-03-01
external_link: ''
---

# Overview

This project is a real-time digital twin system that collects environmental data from a seed propagation lab and visualizes it in a 3D environment.

I was responsible for backend development and Linux server operations, including real-time data processing with MQTT and WebSocket, Docker-based deployment, REST API development, and integration of an LLM chatbot using the Groq API.

---

# Highlights

- Real-time data processing with MQTT and WebSocket
- Linux server administration and Docker deployment
- Development and debugging with Claude Code
- Automation of repetitive operational tasks using Makefile
- LLM chatbot integration with Groq API

---

# Responsibilities

- Backend development
- Linux server setup and maintenance
- Docker-based deployment
- MQTT & WebSocket data processing
- REST API development
- Groq API integration for LLM chatbot

---

# Tech Stack

### Backend
- Java
- Spring Boot

### Database
- MySQL

### Infrastructure
- Linux
- Docker
- Nginx

### Communication
- MQTT
- WebSocket

### AI
- Claude Code
- Groq API

### Collaboration
- Git
- GitHub

---

# Key Contributions

- Built a real-time data pipeline using MQTT and WebSocket.
- Developed REST APIs for collecting and managing environmental data.
- Deployed and managed services in a Linux environment using Docker.
- Connected real-time sensor data with a 3D digital twin dashboard.
- Integrated an LLM chatbot using the Groq API.

---

# AI-Assisted Development

Throughout the project, I used **Claude Code as a development partner** rather than simply a code-generation tool.

- Created FRD and PRD documents to define project scope and functional requirements.
- Debugged MQTT communication and WebSocket synchronization issues by analyzing logs and system architecture with Claude.
- Improved the structure of the 3D dashboard UI through iterative discussions.
- Verified, refined, and tested AI-generated code before integrating it into the project.

This experience taught me how to effectively incorporate generative AI into the software development lifecycle while maintaining code quality and reliability.

---

# Operational Automation

To reduce repetitive operational tasks, I automated server management workflows.

Previously, restarting the production server required executing a long Docker Compose command:

```bash
docker compose -f docker-compose.yml \
-f deploy/docker-compose.prod.yml \
--env-file deploy/.env.prod restart nginx-proxy
```

Using Claude Code, I created a Makefile that simplified the process to:

```bash
make restart
```

This improvement helped:

- Reduce repetitive manual input
- Minimize operational mistakes
- Improve consistency and efficiency in server management

---

# What I Learned

Through this project, I gained hands-on experience in:

- Designing real-time data processing systems
- Linux server administration and Docker deployment
- Applying generative AI to software development and operations
- Automating repetitive tasks
- Validating and refining AI-assisted solutions before production use

These experiences strengthened not only my backend development skills but also my ability to improve operational efficiency through practical engineering solutions.

---

# GitHub

🌱 Repository

https://github.com/capstone-SeedLabSystem/SeedLabDigitalTwin_System
