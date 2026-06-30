---
title: 종자 증식실 디지털 트윈 (SW캡스톤디자인)
summary: 종자 증식실의 환경 데이터를 실시간으로 수집·모니터링하고 3D 디지털 트윈으로 시각화하는 시스템. 환경 시뮬레이션·수확량 예측과 LLM 챗봇(Groq API)을 지원하며, 백엔드 개발과 서버 운영을 담당했습니다.
tags:
  - IoT
  - Backend
  - Capstone
  - Digital Twin
  - LLM
date: 2026-03-01
external_link: ''
---

## 프로젝트 개요

종자 증식실의 환경 데이터를 실시간으로 수집하고 모니터링할 수 있는 시스템 개발 프로젝트에서 **백엔드 개발과 서버 운영**을 담당했습니다.

### 담당 업무

- MQTT와 WebSocket 기반의 실시간 데이터 수집·전송 구조 구현
- Linux 서버 환경 구축 및 Docker 기반 서비스 운영
- 실시간 3D 디지털 트윈 데이터 연동
- 환경 데이터 API 개발 및 데이터 흐름 설계
- Groq API 기반 LLM 챗봇 연동
- 서비스 운영 과정에서 발생하는 서버 및 네트워크 이슈 해결

### AI 활용 경험

개발 과정에서 **Claude Code**를 적극 활용하여 업무 효율을 높였습니다.

- MQTT 통신 오류와 데이터 연동 문제 발생 시 로그와 시스템 구조를 함께 분석하며 원인을 빠르게 파악
- FRD(Product Requirements Document)와 PRD(Functional Requirements Document)를 작성하고 이를 기반으로 기능을 단계적으로 구현
- 3D 디지털 트윈 대시보드 UI 구조를 Claude와 함께 설계하며 화면 구성을 개선
- AI가 제안한 코드와 구조를 그대로 적용하지 않고 직접 검증·수정하며 프로젝트에 반영

### 운영 자동화

반복적으로 수행하던 서버 운영 작업도 자동화했습니다.

기존에는 서버 재배포 시

```bash
docker compose -f docker-compose.yml \
-f deploy/docker-compose.prod.yml \
--env-file deploy/.env.prod restart nginx-proxy
```

와 같은 긴 명령어를 반복 입력해야 했습니다.

Claude와 함께 Makefile을 작성하여

```bash
make restart
```

한 줄의 명령으로 동일한 작업을 수행하도록 개선했습니다.

이를 통해 반복 작업 시간을 줄이고 운영 과정의 실수를 최소화하며 서버 관리 효율을 높였습니다.

### 프로젝트를 통해 얻은 점

- 실시간 데이터 처리 구조와 백엔드 설계 경험
- Linux·Docker 기반 서버 운영 경험
- 생성형 AI를 개발과 운영 업무에 실제 적용한 경험
- 반복 업무 자동화 및 운영 효율 개선 경험
- AI 결과물을 검증·보완하며 협업하는 개발 방식 습득

## GitHub

🌱 Repo: https://github.com/capstone-SeedLabSystem/SeedLabDigitalTwin_System
