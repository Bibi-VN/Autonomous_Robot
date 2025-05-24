# Simulation of Mobile Robot

This project simulates the TIAGo mobile robot in a kitchen environment using Webots and Python.

## Demonstration:
Below are two videos demonstrating the robot's capabilities:

### Video 1: Mapping, Navigation, and Path Planning

The robot follows a predefined trajectory to explore and build a map of the environment. Then, it performs path planing and navigation based on the constructed map.

[Watch Video 1](https://youtu.be/cBmVXozQd8M)

### Video 2: Pick-and-Place Task Execution

The goal is that the robot can autonomously detect, grasp, and transfer three jars from a worktop surface to a designated position on a nearby table.

The solution is designed such that the robot mimics how a human would perform the task. The behavior is structured using a behavior tree and involves the following steps:
1. Move to the worktop
2. Detect the presence of target jars
3. Select and pick one of the detected jars
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
---

## ⚙️ Installation

1. Clone the repository (if applicable):
   ```bash
   git clone https://github.com/Bibi-VN/Mobile_Robot.git
   ```
2. Navigate to the project directory 
   ```bash
   cd ~/Mobile_Robot
   ```
3. Create and activate the Conda environment:  
   This project uses [Miniconda](https://docs.conda.io/en/latest/miniconda.html).

   ```bash
   conda env create -f environment.yml
   conda activate mobile_robots
   ```
## 🚀 Usage
1. Launch the Webots simulation
   ```bash
   webots worlds/kitchen.wbt
   ```
2. Webots Integration to use your Conda environment in Webots:
   Open Webots
   Go to **Tools → Preferences**
   Set **Python command** to the full path of the Conda Python:

   ```bash
   /home/your_username/miniconda3/envs/mobile_robots/bin/python
   ```
   
3. Click the "Play" button in Webots after launching
