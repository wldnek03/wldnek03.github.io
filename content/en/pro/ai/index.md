---
title: A* Algorithm
date: 2024-04-01
image:
  focal_point: 'top'
---

 1. Grid World Display: The Grid World screen is fixed at 930 rows and 850 columns.
 2. Random Walls Button: Pressing this button generates random obstacles in the empty grid cells, based on the M × N × inc obstacle ratio.
 3. User-Defined Obstacles: Users can click to toggle obstacles in the grid manually.
 4. Move Start and Goal Points: The start point is positioned at the top left, and the goal point is at the bottom right, which can be moved by the mouse.
 5. A* Algorithm Execution: After running the A* algorithm, the shortest path is displayed with a yellow line, and the number of explored nodes is outputted.
 6. Change Heuristic Function: Users can choose between Manhattan distance and Euclidean distance for the A* algorithm.
 7. No Shortest Path Found: If the algorithm fails to find a shortest path, an appropriate message is displayed.
 8. Reset Button: Pressing this button resets the grid to its initial state, removing all obstacles.

 Technologies Used
 - Python
 - NumPy
 - Heapq
 - Pygame (for game development and GUI environment)
 - Pgu (GUI library)
 - A* Algorithm (using heuristic functions)
<head>
    <style>
        p {
            text-align: justify;
        }
    </style>
</head>