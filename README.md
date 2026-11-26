
<h1 align="center">👋 Hi, I'm David Ceballos</h1>

<h3 align="center">Mechatronics Engineer | Robotics & Autonomous Systems</h3>

<p align="center">
  Designing, building and integrating intelligent electromechanical systems.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white"/>
  <img src="https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white"/>
  <img src="https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/CAD-555555?style=for-the-badge&logoColor=white"/>
</p>

---

## 👨‍💻 About Me

I'm a Mechatronics Engineer passionate about designing, building, integrating and improving robotic systems.

I currently work as a Field Service Engineer, supporting autonomous mobile robotic systems deployed in large-scale warehouse automation environments.

My engineering experience spans mechanical design, embedded systems, robotic integration, control software, system commissioning and technical troubleshooting.

---

## 🛠️ Technical Expertise

- 🤖 **Robotics:** AMRs, AGVs, industrial robotic arms and system integration.
- 💻 **Software:** Python, C/C++, SQL and TCP/IP communication.
- 🔌 **Embedded Systems:** ESP32, microcontrollers, motor drivers and sensor integration.
- ⚙️ **Mechanical Engineering:** CAD, electromechanical design, rapid prototyping and additive manufacturing.
- 📈 **Control Systems:** PID control, motion control and system validation.

---

## 🚀 Featured Projects


### 🤖 [Robotic PCB Testing Cell](https://github.com/davidrcm1/PCB-Testing-COBOT)

Development and integration of an automated PCB testing cell using a Flexiv Rizon 4 collaborative robotic arm, integrating existing industrial testing equipment into a centralised automation system.

#### 🎬 System Demonstration

<p align="center">
  <img width="46%" src="https://github.com/user-attachments/assets/b314935a-708a-4745-8a0d-cc8f9a267198" />
  &nbsp;&nbsp;&nbsp;
  <img width="46%" src="https://github.com/user-attachments/assets/47f00add-5d25-4169-848b-7f75ca7c57d4" />
</p>

#### ⚙️ System Architecture

```mermaid
flowchart TD
    H[Operator HMI] <--> C[Python Cell Controller]
    C <-->|Serial Communication| M1[PCB Tester 1]
    C <-->|Flexiv RDK| R[Flexiv Rizon 4]
    C <-->|Serial Communication| M2[PCB Tester 2]
    R --> P[PCB Handling and Sorting]
```



#### 🔄 Automated Testing Workflow

```mermaid
flowchart LR
    A[PCB Pickup] --> B[Scanning]
    B --> C[Machine Loading]
    C --> D[Testing]
    D --> E[Machine Unloading]
    E --> F[PASS / FAIL Sorting]
```

The controller independently monitors multiple testing machines, enabling concurrent testing cycles while coordinating access to a shared robotic arm.

#### 📐 Mechanical Design & Prototyping

<p align="center">
  <img height="250" src="https://github.com/user-attachments/assets/87e8e526-d43f-4f46-8088-7491818d277e" />
  &nbsp;&nbsp;&nbsp;
  <img height="250" src="https://github.com/user-attachments/assets/6f4b7fdc-f010-4261-8297-5cbcc678080b" />
  &nbsp;&nbsp;&nbsp;
  <img height="250" src="https://github.com/user-attachments/assets/f23b2757-07dc-4807-bba0-2bd9d71632b7" />
</p>

#### 💻 Controller Application & HMI

<p align="center">
  <img width="45%" src="https://github.com/user-attachments/assets/acaee83c-1137-4506-bf53-7fe8415fe9ed" />
</p>

**Technologies and skills:**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Robotics](https://img.shields.io/badge/Robotics-333333?style=flat-square)
![CAD](https://img.shields.io/badge/CAD-555555?style=flat-square)
![System Integration](https://img.shields.io/badge/System_Integration-0078D4?style=flat-square)

**[📂 View Full Project Documentation & Source Code](https://github.com/davidrcm1/PCB-Testing-COBOT)**


---

### 🎯 [Vision-Based Tracking Turret](https://github.com/davidrcm1/Turret)

Design and development of a custom two-axis pan-and-tilt tracking platform integrating mechanical design, embedded motion control and computer vision.

The system uses an ESP32-S3 to control two NEMA 17 stepper motors through A4988 motor drivers, with a belt-driven mechanical transmission for improved positioning resolution.

#### 📐 Mechanical Design & Prototyping

<p align="center">
  <img height="300" src="https://github.com/user-attachments/assets/9dd3a10e-7bd3-417a-829a-4167d98ed782" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img height="300" src="https://github.com/user-attachments/assets/38680e2d-833d-4190-8e99-febef00e9e46" />
</p>

#### ⚙️ System Architecture

Proposed vision-based closed-loop control architecture:

```mermaid
flowchart TD
    A[Camera] --> B[Computer Vision Processing]
    B --> C[Tracking Error]
    C --> D[Motion Commands]
    D -->|Network Communication| E[ESP32-S3]
    E --> F[Pan Motor Driver]
    E --> G[Tilt Motor Driver]
    F --> H[Pan Stepper Motor]
    G --> I[Tilt Stepper Motor]
    H --> J[Pan-Tilt Platform]
    I --> J
    J -.->|Visual Feedback| A
```

#### 🔌 Electronics & Hardware Integration

<p align="center">
  <img width="1007" height="643" alt="Screenshot 2026-11-26 161642" src="https://github.com/user-attachments/assets/85b9ea78-220b-4b68-a1d5-9de8d633e794" />

</p>

#### 📊 Hardware Configuration

| Component | Specification |
|---|---|
| Microcontroller | ESP32-S3 |
| Actuators | 2 × NEMA 17 stepper motors |
| Motor drivers | 2 × A4988 |
| Pan driven pulley | 142 teeth |
| Tilt driven pulley | 60 teeth |
| Power supply | 12 V DC |
| Manufacturing | CAD and 3D printing |

**Technologies and skills:**

![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![TCP/IP](https://img.shields.io/badge/TCP%2FIP-0078D4?style=flat-square)
![CAD](https://img.shields.io/badge/CAD-555555?style=flat-square)
![3D Printing](https://img.shields.io/badge/3D_Printing-FF6F00?style=flat-square)

![Status](https://img.shields.io/badge/Status-In_Development-yellow?style=flat-square)

**[📂 View Full Project Documentation & Source Code](https://github.com/davidrcm1/Turret)**


---


### 🗺️ [Autonomous Mobile Robot – SLAM & Frontier-Based Exploration](https://github.com/davidrcm1/AMR---SLAMs---Auto-exploration)

Development of a ROS 2-based autonomous mobile robot simulation capable of mapping and exploring unknown environments using LiDAR-based SLAM, autonomous navigation and custom frontier-based exploration algorithms.

The system integrates a differential-drive robot, A* path planning, obstacle avoidance and autonomous navigation goal generation within a custom Gazebo simulation environment.

#### 🎬 Autonomous Exploration Demonstration

<p align="center">
  <img width="46%" src="https://github.com/user-attachments/assets/5d59412f-5fdf-4e9e-8f1c-8fc2bce17d98" />
  &nbsp;&nbsp;&nbsp;
  <img width="46%" src="https://github.com/user-attachments/assets/0076e57d-6cb4-4ce9-b327-87ec29d1f67d" />
</p>

#### ⚙️ System Architecture

```mermaid
flowchart TD
    A[Gazebo Simulation] -->|LiDAR and Odometry| B[SLAM Toolbox]
    B -->|Occupancy Grid| C[Frontier Detector]
    C -->|Frontier Centroids| D[Frontier Explorer]
    D -->|Navigation Goals| E[Nav2]
    B -->|Map| E
    E --> F[Differential Drive Controller]
    F --> A
```

#### 🧠 Autonomous Exploration Algorithm

```mermaid
flowchart TD
    A[Occupancy Grid] --> B[Detect Frontier Cells]
    B --> C[BFS Frontier Clustering]
    C --> D[Calculate Centroids]
    D --> E[Select Eligible Frontier]
    E --> F[A* Path Planning]
    F --> G[Autonomous Navigation]
    G --> A
```

Custom Python-based ROS 2 nodes identify boundaries between explored and unexplored regions, cluster frontier cells using Breadth-First Search and autonomously generate navigation goals.

Previously visited and failed navigation targets are filtered to support continued exploration.


#### 🗺️ Mapping & Visualisation

<p align="center">
  <img width="46%" src="https://github.com/user-attachments/assets/939e101f-3d1f-4253-9869-0f2afddb71d9" />
  &nbsp;&nbsp;&nbsp;
  <img width="46%" src="https://github.com/user-attachments/assets/c5db8c38-f3af-4d12-9669-6c25aeade100" />
</p>

#### 💻 Operator Interface

Custom Python-based HMI for manual robot control, autonomous exploration, system monitoring and occupancy grid export.

<p align="center">
  <img width="65%" src="https://github.com/user-attachments/assets/3bf4fd04-1647-404f-9455-6bcd6ec609eb" />
</p>

**Technologies and skills:**

![ROS2](https://img.shields.io/badge/ROS_2-22314E?style=flat-square&logo=ros&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-F58113?style=flat-square)
![SLAM](https://img.shields.io/badge/SLAM-0078D4?style=flat-square)
![Nav2](https://img.shields.io/badge/Nav2-333333?style=flat-square)
![Path Planning](https://img.shields.io/badge/Path_Planning-00897B?style=flat-square)
![URDF](https://img.shields.io/badge/URDF-555555?style=flat-square)

**[📂 View Full Project Documentation & Source Code](https://github.com/davidrcm1/AMR---SLAMs---Auto-exploration)**

---



### 🫀 [Physiological Pressure Waveform Replicator](https://github.com/davidrcm1/PID-Physiological-Pressure-Waveform-Replicator)

Design and development of a low-cost, Arduino-based closed-loop pressure control system for physiological pressure waveform replication in clinical research applications.

The project combines embedded control, PID feedback control and MATLAB-based physiological waveform processing to reproduce time-varying pressure profiles.

#### ⚙️ Closed-Loop Control Architecture

```mermaid
flowchart LR
    A[Reference Pressure] --> B((Error))
    B --> C[PID Controller]
    C --> D[Pressure Actuation]
    D --> E[Pressure System]
    E --> F[Pressure Measurement]
    F -->|Feedback| B
```

The feedback control system continuously compares the reference pressure waveform against the measured pressure and adjusts the control output to minimise tracking error.

#### 📈 System Development & Experimental Results

<p align="center">
  <img width="46%" src="https://github.com/user-attachments/assets/ee4ad0fe-b115-43e5-be23-fb8d609525c1" />
  &nbsp;&nbsp;&nbsp;
  <img width="46%" src="https://github.com/user-attachments/assets/94660073-00e3-4a32-89ef-45cb077c2824" />
</p>

<p align="center">
  <img width="70%" src="https://github.com/user-attachments/assets/0cad269f-f240-4f41-bc53-06298bc3ddb2" />
</p>

#### 🧮 Physiological Waveform Processing

```mermaid
flowchart TD
    A[Physiological Pressure Dataset] --> B[MATLAB Processing]
    B --> C[Unit Conversion]
    C --> D[Time Scaling and Resampling]
    D --> E[Reference Waveform CSV]
    E --> F[Arduino Controller]
    F --> G[Closed-Loop Pressure Control]
```

MATLAB is used to process physiological pressure datasets, convert pressure units, adjust waveform duration and resample the reference signal for embedded controller execution.


#### 📄 Research Documentation

The project repository includes the thesis report, MATLAB waveform processing script and reference waveform datasets.

[View Engineering Thesis Report](https://github.com/davidrcm1/PID-Physiological-Pressure-Waveform-Replicator/blob/main/ThesisC_z5267332_REPORT.pdf)

**Technologies and skills:**

![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-E16737?style=flat-square)
![PID Control](https://img.shields.io/badge/PID_Control-0078D4?style=flat-square)
![Control Systems](https://img.shields.io/badge/Control_Systems-333333?style=flat-square)
![Signal Processing](https://img.shields.io/badge/Signal_Processing-555555?style=flat-square)
![Biomedical Engineering](https://img.shields.io/badge/Biomedical_Engineering-E63946?style=flat-square)

**[📂 View Full Project Documentation & Research](https://github.com/davidrcm1/PID-Physiological-Pressure-Waveform-Replicator)**

---


## 🔬 Engineering Interests

- 🤖 Autonomous robotic systems
- 💻 Embedded software development
- 👁️ Computer vision
- ⚙️ Electromechanical product development
- 📐 Robotic motion and control systems

---

## 🌐 Connect

📍 Sydney, Australia

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/davidrcm1)
