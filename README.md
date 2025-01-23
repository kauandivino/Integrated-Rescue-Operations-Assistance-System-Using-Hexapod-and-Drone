# Arakdyn: Integrated Rescue Assistance System with Hexapod Robot and Drone

## Overview
The Arakdyn Project was developed to address challenges in rescue operations in hazardous environments, such as natural disasters, structural collapses, and remote, hard-to-reach areas. By combining the robustness of a hexapod robot designed to navigate uneven terrains and the aerial capabilities of a DJI Tello drone equipped with advanced computer vision technologies, the system provides an integrated solution for efficient and safe environmental mapping and monitoring. The use of April Tags as visual markers ensures precision in detection and tracking, essential for the drone’s autonomous navigation and real-time situational mapping.

The integration between the hexapod and the drone is the project's main innovation, enabling both robots to work synchronously to deliver detailed and critical data to rescue teams. While the drone captures aerial information and identifies optimal paths using a screen-divided quadrant system, the hexapod utilizes precise movements to access areas unreachable by other means. The system is designed with a focus on operational efficiency and adaptability, being robust enough to operate under various lighting and terrain conditions, supporting rapid decision-making during emergencies.


## Technologies Used
### Hexapod Robot
* **Components:** ESP32cam, PCA9685, 12 MG90s Servomotors.
* **Locomotion Control:** Wi-Fi system with a web-based interface for commands.
* **Structure:** Modular build with 3D-printed parts.

### DJI Tello Drone
* **April Tags Detection:** Algorithms based on the tag36h11 family.
* **Autonomous Navigation:** Screen divided into 25 quadrants for position tracking.

### Computer Vision Algorithms
* Detect and track April Tags to calculate position and adjust movement.
* Tracking strategy based on the relative position of the tags.

### Communication Protocol:
* Integration between the drone and hexapod through Wi-Fi connectivity.

## Repository Structure
`/Drone`
* Code for detecting April Tags and autonomously controlling the DJI Tello drone.
* Main file: `april_tag_metrics.py`

`/Hexapod`
* Contains the control system for the hexapod robot.
* `/initial_code`: Initial system code (`SIXpackAcessPoint.ino`).
* `/final_code`: Final code with locomotion logic and integration (`Arakdyn_hexapod.ino`).

`/Relatorio`
Technical report detailing the project’s objectives, methodology, technologies, results, and conclusions. Portuguese and English versions

`presentation_slides.pdf`
Weekly pitch presentations and the final presentation
[link to pitch](https://www.canva.com/design/DAGKND1_lDg/3HCiJwd46407NmpLzFFpfw/view?utm_content=DAGKND1_lDg&utm_campaign=designshare&utm_medium=link&utm_source=editor)

`demonstration.mp4`
practical demonstration video of the project in operation

## Installation and Usage
### Prerequisites
1. Hexapod
* Configure the ESP32cam and upload the code available in /Hexapod/final_code/.
* Calibrate the servomotors to ensure precise movements.

2. DJI Tello Drone
* Install the required dependencies
  
`pip install opencv-python apriltag djitellopy numpy`

* Run the script april_tag_metrics.py.
### Execution
1. Connect to the Wi-Fi access point created by the ESP32cam.
2. Start the detection and control system on the drone.
3. Use the web interface to control the hexapod and visualize the environment in real time.

### Results
### Performance Metrics
* **Detection Rate:** 94.03%.
* **False Positive Rate:** 5.97%.
* **Average Position Error:** 77.32 pixels.
* **Average Processing Time:** 0.0034 seconds.

### Highlights
* Precise locomotion of the hexapod on challenging terrains.
* Effective autonomous navigation of the drone, adjusting trajectory based on April Tags.
* Robust system performance under various lighting and environmental conditions.

## Contributors
1. Fabrycio Leite Nakano Almada - fabrycio@discente.ufg.br
2. Kauan Divino Pouso Mariano - kauan@discente.ufg.br
3. Maykon Adriell Dutra - maykonadriell@discente.ufg.br
4. Victor Emanuel da Silva Monteiro - victor_emanuel@discente.ufg.br
