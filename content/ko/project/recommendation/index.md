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
  ## 1번: Grid World 화면 출력 Grid World의 화면은 고정해야 하므로 행을 930, 열을 850으로 고정해서 설정했다.  
  화면의 크기는 눈으로 보았을 때 가장 적절한 크기인 것 같아서 행을 930, 열을 850으로 고정해서 설정한 것이다. 
  그리고 Grid cells의 행과 열의 갯수 M과 N의 default 값은 30 이며, argparse를 이용하여 command line에서 입력받을 수 있도록 하는 것이 조건이므로 parse_args 함수를 이용해 rows의 default값과 cols의 default 값을 30으로 설정하였고 argparse를 통해 --rows 와 --cols 옵션을 추가하여 명령줄에서 입력받을 수 있도록 설정했다. 

  ## 2번: random walls 버튼을 눌러 장애물 랜덤 배치
  랜덤 배치에서는, M ×N × inc obstacle ratio 갯수만큼의 장애물이 비어있는 grid cell에 새롭게 생성되며 inc obstacle ratio의 default값은 0.2로 설정하고 inc obstacle ratio의 값은 argparse를 이용하여 command line에서 옵션으로 입력받을 수 있도록 하는 것이 조건이다. 그래서 python GUI library인 PGU를 사용해서 Random Walls 버튼을 만들었다. 버튼을 클릭하면 랜덤으로 장애물을 생성해야하기 때문에 버튼을 클릭하면 random_obstacles 함수로 이동하여 M ×N × inc obstacle ratio 갯수만큼의 장애물이 비어있는 grid cell에 새롭게 생성하도록 하였다. parse_args 함수를 이용해 inc obstacle ratio의 default값은 0.2로 설정하였고 argparse를 통해 --obstacle_prob 옵션을 추가하여 명령줄에서 입력받을 수 있도록 설정했다. 

  ## 3번: 장애물을 사용자가 직접 배치
  grid world 상에 있는 마우스로 선택한 cell이 비어있다면 gray color로 배경색을 변경하여 장애물로 바꾸고 만약 선택한 ell이 장애물이었다면 toogle 되어 다시 비어있는 cell로 바꾸는 것이 조건이다. 그래서 pygame의 while문에 마우스 클릭 이벤트 처리 코드를 작성하였다. 즉, 왼쪽 마우스를 클릭시 그리드에서 장애물을 toogle하도록 코드를 작성했다. 

  ## 4번: 시작 지점, 목표 지점 마우스로 옮기기
  시작지점과 목표지점은 초기에 랜덤하게 또는 고정 위치에 S와G로 표시되도록하고, 사용자 마우스 클릭을 통해 이동될 수 있도록 하는 것이 조건이다. 시작지점과 목표지점을 고정 위치에 지정하기로 결정하여 draw_gird 함수에 시작지점은 왼쪽 상단, 목표지점은 오른쪽 하단에 위치하도록 설정했다. 그리고 마우스 클릭을 통해 이동될 수 있도록 설정하기 위해 while문에 마우스 클릭 이벤트 처리 코드를 작성했다. 장애물을 사용자가 직접 배치할 때 마우스의 왼쪽을 클릭 시 작동한다. 혼동을 줄이기 위해 시작 지점, 목표 지점 이동은 마우스의 오른쪽을 클릭 시 작동하도록 했다. 

  ## 5번: A* 알고리즘 수행 후 최단거리 yellow line으로 표시, 콘솔 화면에 해를 탐색할 때까지의 총 explored nodes 개수 출력
  Start A* Search 버튼 클릭 시 S와 G에 A* search를 수행하여, 최단 경로를 찾을 경우 해당 경로를 yellow line으로 표시하며 콘솔 화면에 해를 탐색할 때까지의 총 explored nodes 개수를 출력하는 것이 조건이다. 그래서 python GUI library인 PGU를 사용해서 Start A* Search 버튼을 만들었다. 버튼을 클릭하면 A* 알고리즘을 수행해야 하므로 버튼을 클릭하면 astar함수로 이동하여 A* 알고리즘을 수행하게 하였다. astar 함수 내에서 exploredd_nodes 변수를 사용하여 탐색 된 총 노드 수를 카운트하였고 start_search 함수에서 astar 함수를 호출하여 콘솔에 탐색된 총 노드 수를 출력하게 만들었다. 그리고 A* 알고리즘 수행을 하여 최단 경로를 찾았으면 해당 경로를 yellow line으로 표시해야 하므로 draw_path 함수를 사용하여 작동하도록 했다. 

  ## 6번: 휴리스틱 함수를 바꿔서 A*알고리즘 수행
  휴리스틱 함수로 현재 node의 위치와 gold node 위치 간의 Manhattan 거리, Euclidean 거리 두 가지 중 하나를 선택하여 수행할 수 있도록 하는 것이 조건이다. 그래서 휴리스틱 함수를 선택할 수 있는 라디오 버튼을 python GUI library인 PGU를 사용하여 만들었다. 선택된 휴리스틱 함수에 따라 A* 알고리즘을 수행해야 하므로 버튼을 클릭 시 heuristic 함수로 이동하여 각 함수에 맞는 A* 알고리즘을 수행하도록 작성하였다. 아무것도 선택하지 않았을 경우에는 default 값으로 Manhattan을 설정해두어 Manhattan 방식으로 알고리즘이 수행된다.

  ## 7번: 최단거리 해가 없을 때 수행
  만약 A* 알고리즘이 최단 경로를 찾지 못했을 경우 최단 경로가 없다는 메시지를 콘솔에 출력하도록 작성하였다. 그리고 경로를 찾지 못했을 시 가장 낮은 f(n)을 가진 노드까지의 경로를 GUI에 표시하라고 하였으므로 draw_path 함수를 호출하여 경로를 표시하도록 했다.
   
  ## 8번: reset 버튼을 눌렀을 때 수행
  python GUI library인 PGU를 사용하여 Reset 버튼을 만들었다. Reset 버튼이 눌리면 장애물이 모두 사라진 초기 상태의 그리드가 나와야 하므로 그리드를 초기 상태로 리셋하고 그리드를 업데이트하도록 작성했다. 

  ## 사용 기술
  - Python
  - NumPy
  - Heapq
  - Pygame (게임 개발 및 GUI 환경)
  - Pgu (GUI 라이브러리)
  - A 알고리즘* (휴리스틱 함수 사용)
---
