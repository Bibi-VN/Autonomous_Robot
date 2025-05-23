# Simulation of Mobile Robot

This project simulates the TIAGo mobile robot in a kitchen environment using Webots and Python.

## Demonstration:
Below are two videos demonstrating the robot's capabilities:

### Video 1: Mapping, Navigation, and Path Planning

The robot follows a predefined trajectory to explore and build a map of the environment. Then, it perfroms path planing and navigation based on the constructed map.

[Watch Video 1](https://youtu.be/cBmVXozQd8M)

### Video 2: Pick-and-Place Task Execution

The goal is that the robot can autonomously detect, grasp, and transfer three jars from a worktop surface to a designated position on a nearby table.

The solution is designed such that the robot mimics how a human would perform the task. The behavior is structured using a behavior tree and involves the following steps:
1. Move to the worktop
2. Detect the presence of target jars
3. Select and pick one of detected jars
4. Transfer it to the designated position on the table
5. Repeat until the task is complete

[Watch Video 2](https://youtu.be/2DOx8iX4RRk)

## Project Structure
``` 
root/
├── controllers/                    # Robot control scripts
│   ├── Tiago_controller.py         # Main robot control logic
│   ├── navigation.py               # Autonomous navigation based on provided waypoints
│   ├── mapping.py                  # Environment scanning and map building
│   ├── planning.py                 # Path planning for navigation
│   ├── set_waypoint.py             # Waypoint setting utility
│   ├── manipulation.py             # Pick-and-place logic
│   ├── recognition.py              # Object recognition for picking
│   ├── object_selector.py          # Logic for selecting objects to manipulate
│   └── straight_line_navigation.py # Straight-line navigation supporting the picking process
├── worlds/                         # Webots simulation world
│   └── kitchen.wbt
├── assets/                         # README images or visualizations
├── environment.yml                 # Conda environment configuration
└── README.md
```
