---
title: 종자 증식실 환경 모니터링 시스템 (SW캡스톤디자인)
date: 2026-03-01
image:
  focal_point: 'top'
---

[🌱 GitHub Repository](https://github.com/capstone-SeedLabSystem/SeedLabDigitalTwin_System)

종자 증식실은 우수 품종의 종자를 체계적으로 생산·관리하는 재배 시설로, 종자 품질이 생육 환경에 직접 좌우되어 실시간 환경 관리가 필수적입니다. 본 프로젝트는 센서 기반 데이터 수집부터 임계값 알림, 3D 디지털 트윈 시각화, 환경 시뮬레이션까지 증식실 운영 전반을 통합 관리하는 시스템이며, 저는 **백엔드 개발과 서버 운영**을 담당하고 있습니다.

**주요 기능**

- **실시간 환경 모니터링** — 대기 온도·습도, 토양 수분·온도 센서 데이터를 5분 주기로 수집해 증식실별 현황을 대시보드에 표시
- **3D 디지털 트윈** — 증식실을 3D로 시각화하고 로트·센서·중계기를 인터랙티브하게 조회, 임계값 이탈 시 영역 색상 변화
- **임계값 알림** — 임계값 이탈·센서 이상·통신 끊김을 감지해 웹에서 실시간 알림 제공
- **환경 시뮬레이션 · 수확량 예측** — 온도·습도·일사량·CO₂ 등 환경 조건을 시뮬레이션해 권장 환경·수확량 예측
- **LLM 챗봇** — 자연어로 증식실 환경 데이터를 질의응답하고, 작물별 최적 온도·습도 등 권장 생육 환경을 안내 (Groq API 기반)
- **로트 · 생육 관리** — 품종별 구획(로트) 단위 생육 단계·수량·상태 추적 및 변경 이력 관리
- **센서 데이터 그래프 · 리포트** — 기간별 시계열 조회, 시간별/일별 집계 그래프·리포트

![자연어로 작물 적정 환경을 안내하는 LLM 챗봇 "농업 AI 도우미"](chatbot.png)

**담당 역할 — 백엔드 & 서버 운영**

- Spring Boot 기반 증식실·로트·센서·알림 도메인 REST API와 JWT 인증/인가(Viewer·Admin 권한) 구현
- 센서 → MQTT(Mosquitto) → RabbitMQ → 저장·알림·실시간 푸시로 이어지는 데이터 파이프라인 설계, 메시지 큐 버퍼링으로 데이터 유실 방지
- TimescaleDB로 대량 센서 데이터를 적재하고 기간별 집계 조회 최적화
- Docker 기반 배포 환경 구성 및 서버 운영·모니터링

**트러블슈팅 — 서버 운영 안정화**

협업 초기, 정해진 절차 없이 배포가 진행되며 운영 장애가 반복 발생했습니다.

- **401 Unauthorized** — API 배포 중 DB 비밀번호가 변경되어 기존 인증 토큰 연결이 끊김
- **502 Bad Gateway** — Nginx가 중지된 채 방치되어 리버스 프록시가 응답하지 못함
- **서버 무응답** — 배포 후 백엔드 프로세스를 재가동하지 않아 요청이 처리되지 않음

서버 로그 추적·프로세스 상태 점검으로 원인을 특정해 직접 복구했고, 재발 방지를 위해 서버 접근·배포 창구를 단일화하고 배포 전 DB 접속 정보 검증 절차를 문서화해 팀에 공유했으며, 반복 점검 작업을 Shell Script로 자동화해 운영 안정성을 높였습니다.

**사용 기술**

- Backend: Java / Spring Boot, Spring Data JPA, Spring Security (JWT)
- Database: PostgreSQL / TimescaleDB
- Messaging · IoT: MQTT (Mosquitto), RabbitMQ
- Realtime: WebSocket (STOMP)
- Frontend: React, Three.js (3D 디지털 트윈)
- Infra: Docker / Docker Compose, Nginx
- 협업: Git / GitHub
<head>
    <style>
        p {
            text-align: justify;
        }
    </style>
</head>
