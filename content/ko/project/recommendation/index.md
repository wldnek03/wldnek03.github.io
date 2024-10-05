---
title: A* Algorithm
summary: M×N Gridworld에서 장애물이 랜덤하게 배치되고, 시작 지점에서 장애물을 피해 목표 지점까지 도달하는 최단 경로를 찾는 A* 알고리즘을 구현하고 이를 GUI 환경에서 시뮬레이션함.
tags:
  - AI
  - A*
  - Numpy
date: 2024-04-01
external_link: http://github.com
description: |
  1. Grid World 화면 출력: Grid World의 화면은 행 930, 열 850으로 고정.
  2. random walls 버튼을 눌러 장애물 랜덤 배치: M × N × inc obstacle ratio 갯수만큼의 장애물이 비어있는 grid cell에 새롭게 생성.
  3. 장애물을 사용자가 직접 배치: 클릭하여 장애물을 토글할 수 있도록 구현.
  4. 시작 지점과 목표 지점 마우스로 옮기기: 시작지점은 왼쪽 상단, 목표지점은 오른쪽 하단에 위치.
  5. A* 알고리즘 수행 후 최단거리 표시: 최단 경로를 yellow line으로 표시하고 explored nodes 개수 출력.
  6. 휴리스틱 함수를 바꿔서 A* 알고리즘 수행: Manhattan 거리, Euclidean 거리 선택 가능.
  7. 최단거리 해가 없을 때 수행: 최단 경로를 찾지 못했을 경우 메시지 출력.
  8. reset 버튼을 눌렀을 때: 장애물이 모두 사라진 초기 상태로 리셋.
  
  ## 사용 기술
  - Python
  - NumPy
  - Heapq
  - Pygame (게임 개발 및 GUI 환경)
  - Pgu (GUI 라이브러리)
  - A 알고리즘* (휴리스틱 함수 사용)
---