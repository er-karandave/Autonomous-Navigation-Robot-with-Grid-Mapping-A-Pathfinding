# Autonomous-Navigation-Robot-with-Grid-Mapping-A-Pathfinding
Autonomous mobile robot with real-time grid mapping using ultrasonic sensors and A* pathfinding algorithm. Features obstacle detection, dynamic path replanning, and ROS 2 integration for autonomous navigation in unknown environments.
# Project Overview
A mobile robot that:
Maps its environment using ultrasonic/LiDAR sensors to build a 2D occupancy grid
Detects obstacles in real-time
Plans optimal paths using A* algorithm
Navigates autonomously to target coordinates
Replans paths dynamically when new obstacles are detected

# Technology Stack
Hardware (Choose one):
Option A (Budget): Arduino/ESP32 + HC-SR04 Ultrasonic Sensors (3x) + Motor Driver + DC Motors
Option B (Advanced): Raspberry Pi + RPLiDAR A1 + Motor Driver + DC Motors
Option C (Simulation Only): ROS 2 + Gazebo (no hardware needed)

# Software:
Core: Python 3.10+ or C++
ROS 2: Humble/Iron (for robot control and sensor integration)
Algorithms: A* Pathfinding, Occupancy Grid Mapping
Visualization: Matplotlib, RViz2 (ROS 2)
Optional: OpenCV for camera-based obstacle detection


autonomous-robot-navigation/
├── README.md
├── requirements.txt
├── src/
│   ├── mapping/
│   │   ├── occupancy_grid.py          # 2D grid map generation
│   │   ├── sensor_fusion.py           # Ultrasonic/LiDAR data processing
│   │   └── obstacle_detection.py      # Real-time obstacle identification
│   ├── pathfinding/
│   │   ├── astar.py                   # A* algorithm implementation
│   │   ├── dijkstra.py                # Dijkstra's algorithm (comparison)
│   │   └── path_planner.py            # High-level path planning logic
│   ├── control/
│   │   ├── robot_controller.py        # Motor control & movement
│   │   ├── pid_controller.py          # Smooth motion control
│   │   └── kinematics.py              # Differential drive kinematics
│   ├── visualization/
│   │   ├── map_visualizer.py          # Real-time map display
│   │   └── path_visualizer.py         # Path visualization
│   └── main.py                        # Main execution loop
├── ros2_ws/                           # ROS 2 workspace (optional)
│   ├── src/
│   │   ├── robot_bringup/             # Launch files
│   │   ├── robot_navigation/          # Navigation nodes
│   │   └── robot_description/         # URDF robot model
├── simulations/
│   ├── gazebo_world/                  # Gazebo simulation environment
│   └── test_maps/                     # Predefined test maps
└── docs/
    ├── algorithm_explanation.md
    ├── hardware_setup.md
    └── demo_videos/
