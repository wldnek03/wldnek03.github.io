---
title: DrowsyGuard — Real-time Multi-signal Focus Management System
date: 2026-05-27T00:45:00+09:00
image:
  focal_point: 'top'
---

[🔥 GitHub Repository](https://github.com/wldnek03/DrowsyGuard)

DrowsyGuard is a Raspberry Pi 5 based system that detects drowsiness during studying/working and helps users actively recover. It fuses three signals — camera (eyes/yawn), environment (temperature/pressure), and posture (distance) — to compute a unified drowsiness risk score. Beyond a simple alarm, it requires the user to gaze at the camera to dismiss the warning, then guides them through a stretching routine accompanied by classical music. Per-session statistics are persisted to CSV and visualized through a Flask web dashboard.

**Key Features**

- **3-axis fusion drowsiness detection** — Combines eye closure (EAR), environment (temperature/pressure), and posture (ultrasonic distance) signals into a single 0–100% risk score
- **Camera gaze-based dismissal** — No simple button dismissal. User must gaze at the camera for 2 seconds; the OLED shows a progress bar as visual feedback
- **Stretching guide + classical music** — A 30-second routine (neck rolls / stretch / hydration) guided on OLED while the buzzer plays Beethoven's "Ode to Joy" → Mozart's "Twinkle Twinkle" → "Edelweiss" via PWM
- **Personalized EAR calibration** — At session start, samples 3 seconds of the user's open-eye EAR; sets the personal drowsiness threshold to 75% of the average (compensates for individual eye-shape differences)
- **Time-of-day risk weighting** — Applies multipliers automatically: after-lunch (×1.20), early morning (×1.30), late night (×1.15)
- **Yawn detection (MAR)** — Computes Mouth Aspect Ratio to count yawns and increment the risk score
- **Session-based operation + CSV logging** — Start/stop with a button; per-session stats (study time, caution / danger / yawn counts) auto-saved to CSV
- **Tiered LED + buzzer alarms** — NORMAL (green) / CAUTION (yellow + short beep) / DANGER (red + repeating alarm); environment-risk alarm differentiated by lower tone (330 Hz)
- **OLED 3-screen toggle (joystick)** — Dashboard / Environment / Posture+Eye real-time display
- **Web dashboard (Flask + Chart.js)** — Visualizes daily study time, hourly drowsiness occurrence, and recent sessions on phone/laptop

**Role — Solo Personal Project (Full-stack)**

Designed and built the entire system alone: concept → circuit design/wiring → firmware / computer vision → state machine → web dashboard.

**Troubleshooting**

- **Raspberry Pi 5 GPIO incompatibility** — `RPi.GPIO` is incompatible with the Pi 5's RP1 chip, causing `Cannot determine SOC peripheral base address`. Resolved by swapping to `rpi-lgpio`, a drop-in compatible library, with zero code changes
- **Gaze-release counter reset bug** — When the user gazed at the camera, the eye-closure counter dropped, causing `status` to fall `DANGER → CAUTION → NORMAL` and resetting `release_frames` to 0, preventing entry into the stretching state. Introduced a `pending_release` flag so that once DANGER is entered, the gaze counter keeps accumulating until 60 frames are reached
- **dlib face-detection loss on wide yawn** — When the user opened their mouth widely, dlib's face detector failed to detect the face, resetting the yawn counter. Modified the logic to retain the counter while the face is briefly lost and reset only if loss exceeds 0.5 seconds
- **Passive buzzer misclassification** — Initially mistook the 3-pin passive buzzer for an active type and controlled it via `LED.on()`, producing no sound. Switched to `PWMOutputDevice` with 50% duty cycle to drive PWM directly, restoring full tonal output

**Tech Stack**

- **Language**: Python 3.13
- **Computer Vision**: OpenCV + dlib (68 facial landmarks, EAR + MAR)
- **Camera**: Picamera2 (libcamera)
- **GPIO**: gpiozero + rpi-lgpio (Pi 5 compatible)
- **OLED**: luma.oled (SSD1306, I2C)
- **I2C sensors**: smbus2 (BMP180)
- **Web**: Flask + Chart.js
- **Hardware**: Raspberry Pi 5, Pi Camera (OV5647), OLED (SSD1306), BMP180, HC-SR04, LED ×3, Passive Buzzer, Tactile Switch, Joystick
- **OS**: Raspberry Pi OS Bookworm

<head>
    <style>
        p {
            text-align: justify;
        }
    </style>
</head>
