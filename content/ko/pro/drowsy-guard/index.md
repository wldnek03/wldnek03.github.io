---
title: DrowsyGuard — 실시간 다중 신호 기반 집중력 관리 시스템
date: 2026-05-27T00:45:00+09:00
image:
  focal_point: 'top'
---

[🔥 GitHub Repository](https://github.com/wldnek03/DrowsyGuard)

DrowsyGuard는 학습/작업 중 졸음을 감지하고 능동적으로 회복할 수 있도록 돕는 라즈베리파이 5 기반 시스템입니다. 카메라(눈/하품), 환경(온도/기압), 자세(거리) 세 가지 신호를 융합해 졸음 위험도를 산출하고, 단순 경보를 넘어 카메라 응시 해제 + 스트레칭 가이드 + 클래식 음악으로 학습자가 능동적으로 회복하도록 유도합니다. 매 세션 통계를 CSV로 누적하고 Flask 기반 웹 대시보드로 시각화합니다.

**주요 기능**

- **3축 융합 졸음 감지** — 눈 감김(EAR), 환경(온도/기압), 자세(초음파 거리) 신호를 가중합하여 0~100% 위험도 산출
- **카메라 응시 해제** — 단순 버튼 해제 X. 카메라 정면 2초 응시해야 경보 해제, OLED 진행바로 시각 피드백
- **스트레칭 가이드 + 클래식 음악** — 목 돌리기 / 기지개 / 물 마시기 30초 루틴을 OLED로 안내하고 베토벤 환희의 송가 → 모차르트 작은 별 → 에델바이스를 부저 PWM으로 자동 재생
- **개인화 EAR 캘리브레이션** — 세션 시작 후 3초 응시로 본인 눈 EAR 평균 측정 → 평균의 75%를 개인 임계값으로 자동 설정 (눈 크기 차이 보정)
- **시간대별 위험 가중치** — 점심 후(×1.20) · 새벽(×1.30) · 늦은 밤(×1.15) 시간대 졸음 위험을 자동 가중
- **하품 감지 (MAR)** — 입 벌림 비율을 계산해 하품 횟수 카운트 및 위험도 가산
- **세션 기반 운영 + CSV 누적** — 버튼으로 시작/종료, 매 세션 통계(공부 시간, 주의·위험·하품 횟수)를 CSV에 자동 저장
- **단계별 LED + 부저 경보** — NORMAL(초록) / CAUTION(노랑·짧은 비프) / DANGER(빨강·반복 경보), 환경 위험 시 낮은 톤(330Hz)으로 차별화
- **OLED 3화면 전환 (조이스틱)** — Dashboard / Environment / Posture+Eye 실시간 정보 표시
- **웹 대시보드 (Flask + Chart.js)** — 스마트폰/노트북에서 일별 공부 시간, 시간대별 위험 발생, 최근 세션 등을 차트로 시각화

**담당 역할 — 개인 프로젝트 전체 개발**

기획 → 회로 설계/결선 → 펌웨어/영상처리 → 상태머신 → 웹 대시보드까지 모두 단독 개발했습니다.

**트러블슈팅**

- **라즈베리파이 5 GPIO 호환성** — RPi.GPIO가 Pi 5의 RP1 칩과 호환되지 않아 `Cannot determine SOC peripheral base address` 발생. 드롭인 호환 라이브러리 `rpi-lgpio`로 교체해 코드 수정 없이 해결
- **응시 해제 카운트 리셋 버그** — 카메라 응시 시 눈 감김 카운트가 줄어들어 status가 `DANGER → CAUTION → NORMAL`로 떨어질 때 `release_frames`가 0으로 리셋되어 스트레칭 진입 실패. `pending_release` 플래그를 도입해 한 번 DANGER 진입하면 응시 60프레임 도달까지 카운트가 유지되도록 상태머신 수정
- **dlib 얼굴 인식 손실** — 입을 크게 벌리면 dlib detector가 얼굴을 못 잡아 하품 카운트가 리셋되는 문제. 얼굴 인식 실패 시(MAR=None) 카운트를 유지하고 0.5초 이상 손실 시에만 리셋하도록 로직 변경
- **부저 동작 불량** — passive 부저인데 처음에 active 부저로 오판해 LED.on()으로 제어 → 무음. `PWMOutputDevice` + duty cycle 50%로 PWM 신호를 직접 제어하도록 수정하여 해결

**사용 기술**

- **언어**: Python 3.13
- **영상 처리**: OpenCV + dlib (68 facial landmarks, EAR + MAR)
- **카메라**: Picamera2 (libcamera)
- **GPIO**: gpiozero + rpi-lgpio (Pi 5 호환)
- **OLED**: luma.oled (SSD1306, I2C)
- **I2C 센서**: smbus2 (BMP180)
- **웹**: Flask + Chart.js
- **하드웨어**: Raspberry Pi 5, Pi Camera (OV5647), OLED (SSD1306), BMP180, HC-SR04, LED ×3, Passive Buzzer, Tactile Switch, Joystick
- **OS**: Raspberry Pi OS Bookworm

<head>
    <style>
        p {
            text-align: justify;
        }
    </style>
</head>
