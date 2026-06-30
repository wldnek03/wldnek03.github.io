---
title: 종자 증식실 디지털 트윈 (SW캡스톤디자인)
summary: 종자 증식실의 환경 데이터를 실시간으로 수집·모니터링하고 3D 디지털 트윈으로 시각화하는 시스템입니다. MQTT·WebSocket 기반 실시간 데이터 처리, Linux 서버 운영, Docker 배포, LLM 챗봇(Groq API)을 구현했으며, Claude Code를 활용해 개발 생산성과 운영 효율을 개선했습니다.
tags:
  - IoT
  - Backend
  - Capstone
  - Digital Twin
  - LLM
date: 2026-03-01
external_link: ''
---

# 프로젝트 개요

종자 증식실의 환경 데이터를 실시간으로 수집하고 3D 공간에서 모니터링할 수 있는 디지털 트윈 시스템입니다.

백엔드 개발과 Linux 서버 운영을 담당했으며, MQTT와 WebSocket 기반 실시간 데이터 처리, Docker 기반 서비스 운영, 환경 데이터 API 개발, Groq API 기반 LLM 챗봇 연동을 구현했습니다.

---

# Highlights

- MQTT · WebSocket 기반 실시간 데이터 처리
- Docker · Linux 서버 운영 및 배포
- Claude Code를 활용한 개발 및 디버깅
- Makefile 기반 반복 운영 작업 자동화
- Groq API 기반 LLM 챗봇 구현

---

# Role

- Backend 개발
- Linux 서버 구축 및 운영
- Docker 기반 서비스 배포
- MQTT · WebSocket 기반 실시간 데이터 처리
- REST API 개발
- Groq API 기반 LLM 챗봇 연동

---

# Tech Stack

### Backend
- Java
- Spring Boot

### Database
- MySQL

### Infra
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

# 주요 구현 내용

- MQTT와 WebSocket을 이용한 실시간 센서 데이터 수집 및 전송
- Docker 기반 서비스 운영 환경 구축 및 Linux 서버 관리
- 환경 데이터 조회 및 처리 API 개발
- 실시간 데이터를 3D 디지털 트윈과 연동
- Groq API를 활용한 LLM 챗봇 기능 구현

---

# AI 활용 경험

개발 과정에서 **Claude Code를 단순 코드 생성 도구가 아닌 개발 파트너**로 활용했습니다.

- FRD와 PRD를 작성하여 기능 요구사항과 개발 범위를 체계적으로 설계
- MQTT 통신 오류와 WebSocket 데이터 연동 문제 발생 시 로그와 시스템 구조를 함께 분석하며 원인을 빠르게 파악
- 3D 디지털 트윈 대시보드 UI 구조를 설계하고 개선
- AI가 제안한 코드와 구조를 그대로 적용하지 않고 직접 검증·수정한 뒤 프로젝트에 반영

이를 통해 생성형 AI를 활용해 개발 생산성을 높이면서도 결과를 검증하는 개발 방식을 익혔습니다.

---

# 운영 자동화

개발 이후 서버 운영 과정에서 반복적으로 수행하던 작업도 자동화했습니다.

기존에는 서버 재시작 시마다 아래와 같은 긴 Docker Compose 명령어를 직접 입력해야 했습니다.

```bash
docker compose -f docker-compose.yml \
-f deploy/docker-compose.prod.yml \
--env-file deploy/.env.prod restart nginx-proxy
```

Claude Code와 함께 Makefile을 작성하여

```bash
make restart
```

한 줄의 명령으로 동일한 작업을 수행하도록 개선했습니다.

이를 통해

- 반복 입력을 줄이고
- 작업 실수를 최소화하며
- 서버 운영 효율을 높일 수 있었습니다.

---

# 프로젝트를 통해 배운 점

이번 프로젝트를 통해

- 실시간 데이터 처리 구조 설계
- Linux · Docker 기반 서버 운영
- 생성형 AI를 활용한 개발 및 운영 자동화
- 반복 업무 개선 경험
- AI 결과를 검증하고 보완하며 활용하는 협업 방식

을 경험하며, 개발뿐 아니라 운영 효율까지 고려하는 문제 해결 역량을 기를 수 있었습니다.

---

# GitHub

🌱 Repo

https://github.com/capstone-SeedLabSystem/SeedLabDigitalTwin_System
