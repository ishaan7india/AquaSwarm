# AquaSwarm V0.1
### Cleaner Water. A Greener Future.

**AquaSwarm** is a robotic water-surface cleanup project designed to help tackle floating plastic pollution in lakes and other water bodies.

V0.1 focuses on developing the technical foundation for a remotely controlled aquatic cleanup robot, combining a twin-hull floating platform, camera-based monitoring, wireless communication, dual-motor propulsion and a front-mounted waste collection mechanism.

The project aims to make aquatic waste collection more accessible through practical robotics and modular engineering.

![AquaSwarm V0.1 – Project Overview](assets/AquaSwarm%20V0.1%20Lake%20Cleanup%20Overview%281%29.png)

> **Small robot. Big impact.**

---

## Table of Contents

- [The Problem](#the-problem)
- [Our Solution](#our-solution)
- [Project Objectives](#project-objectives)
- [System Architecture](#system-architecture)
- [Hardware Architecture](#hardware-architecture)
- [Propulsion System](#propulsion-system)
- [Floating Platform and Hull Design](#floating-platform-and-hull-design)
- [Waste Collection Mechanism](#waste-collection-mechanism)
- [Camera and Live Monitoring](#camera-and-live-monitoring)
- [Communication and Remote Control](#communication-and-remote-control)
- [Power System](#power-system)
- [Operating Sequence](#operating-sequence)
- [Preliminary Bill of Materials](#preliminary-bill-of-materials)
- [Technical Feasibility](#technical-feasibility)
- [Risk Analysis](#risk-analysis)
- [Estimated Budget](#estimated-budget)
- [Development Roadmap](#development-roadmap)
- [Future Vision – AquaSwarm V8](#future-vision--aquaswarm-v8)
- [Current Project Status](#current-project-status)
- [Acknowledgements](#acknowledgements)

---

## The Problem

Plastic pollution is an increasing concern for aquatic environments. Floating bottles, wrappers and other waste can accumulate on the surfaces of lakes and rivers, affecting the surrounding ecosystem and making cleanup difficult.

Conventional cleanup often requires manual effort, regular maintenance and access to the affected areas.

The problem inspired a simple question:

**Can we use accessible robotics to make floating-waste collection more efficient?**

![Newspaper-style research visuals about lake pollution](assets/Torn%20Headlines%20on%20Lake%20Pollution%281%29.png)

AquaSwarm explores this idea through a robotic platform designed specifically for surface-level waste collection.

## Our Solution

AquaSwarm V0.1 is a proposed remotely controlled robotic platform that can navigate across the water surface and collect accessible floating debris.

The initial design uses a catamaran configuration, with two parallel hulls supporting a central electronics platform and a front-mounted mesh collection attachment.

The system is planned around the following features:

- Twin-hull floating platform.
- Raspberry Pi 4 for main processing.
- Arduino Uno for motor control.
- Camera-based live monitoring.
- Local Wi-Fi remote operation.
- Independent left and right propulsion motors.
- Removable front-mounted mesh collector.
- Rechargeable battery-based power system.

![AquaSwarm V0.1 – Concept render](assets/AquaSwarm%20Lake%20Cleanup%20Catamaran%281%29.png)

**Important:** AquaSwarm V0.1 is currently at the concept, research and technical-planning stage. The visuals represent the proposed design, not a completed or tested physical prototype.

## Project Objectives

The initial objectives of AquaSwarm are:

1. Develop a stable floating robotic platform.
2. Establish a practical remote-control system.
3. Integrate live camera monitoring.
4. Research suitable propulsion methods.
5. Design a lightweight floating-waste collection mechanism.
6. Develop a modular electronics and power architecture.
7. Establish a foundation for future autonomous features.

The initial version prioritises reliable remote operation and basic collection rather than attempting full autonomy immediately.

---

## System Architecture

The proposed architecture divides AquaSwarm into separate subsystems that communicate with one another.

![AquaSwarm V0.1 – System Architecture](assets/AquaSwarm%20V0.1%20System%20Architecture%281%29.png)

### Main processing – Raspberry Pi 4

The Raspberry Pi 4 acts as the primary processing and communication unit.

Its proposed responsibilities include:

- Hosting the browser-based control dashboard.
- Managing local Wi-Fi communication.
- Receiving operator commands.
- Managing camera streaming.
- Communicating with the Arduino.
- Handling system monitoring.
- Providing a foundation for future AI-based processing.

### Hardware control – Arduino Uno

The Arduino Uno is responsible for lower-level hardware control.

Its proposed responsibilities include:

- Receiving commands from the Raspberry Pi.
- Controlling motor direction and speed.
- Interfacing with the motor driver.
- Managing basic hardware inputs.
- Stopping propulsion if communication is lost.

### Communication between controllers

The proposed connection between the Raspberry Pi and Arduino is UART serial communication.

This separates higher-level processing from direct hardware control.

![AquaSwarm Controller Architecture](assets/AquaSwarm%20Controller%20Architecture%20Infographic%281%29.png)

---

## Hardware Architecture

The hardware is divided into several functional groups.

| Component | Proposed role |
|---|---|
| Raspberry Pi 4 | Main processing and communication |
| Arduino Uno | Motor and hardware control |
| Camera module | Live video monitoring |
| Motor drivers / ESCs | Propulsion control |
| Two propulsion motors | Movement and steering |
| Battery system | Main power source |
| Voltage regulators | Regulated power distribution |
| Floating hulls | Buoyancy and stability |
| Mesh collector | Floating-waste collection |

The exact components and specifications will be finalised during the hardware-development phase.

---

## Propulsion System

AquaSwarm V0.1 explores a dual-motor propulsion configuration.

The proposed arrangement places one propulsion unit on each side of the platform. This allows the robot to use differential thrust for steering.

### Differential thrust

- **Forward:** Both motors provide forward thrust.
- **Backward:** Both motors provide reverse thrust.
- **Turn left:** The right motor provides greater thrust than the left.
- **Turn right:** The left motor provides greater thrust than the right.
- **Stop:** Both motors stop.

![AquaSwarm V0.1 – Propulsion Research](assets/AquaSwarm%20V0.1%20Propulsion%20Research%281%29.png)

### Propulsion options considered

Three broad approaches were explored:

1. Waterproof DC motors with propellers.
2. Brushless underwater thrusters.
3. A single motor with a separate rudder.

The final selection will depend on thrust requirements, power consumption, cost, waterproofing and motor-driver compatibility.

---

## Floating Platform and Hull Design

The proposed floating structure uses a **catamaran configuration**.

A catamaran consists of two parallel hulls connected by a central structure.

This arrangement was selected as the preferred concept because it provides:

- A wide floating platform.
- Space for central electronics.
- Room for a front collection attachment.
- A practical layout for two propulsion units.
- Opportunities for modular construction.

![AquaSwarm V0.1 – Hull Design Research](assets/AquaSwarm%20V0.1%20Hull%20Design%20Infographic%281%29.png)

### Buoyancy and stability

The floating platform must support the total mass of:

- Hull structures.
- Electronics and enclosure.
- Battery system.
- Motors and propulsion components.
- Collection mechanism.
- Collected waste.

The displacement and buoyancy requirements will need to be calculated using the final component weights and hull dimensions.

The centre of gravity, hull spacing and freeboard will also need to be considered before construction.

---

## Waste Collection Mechanism

A major part of AquaSwarm is its proposed front-mounted waste collection system.

The initial concept uses a removable mesh collector that allows water to drain while retaining floating debris.

![AquaSwarm V0.1 – Waste Collection Research](assets/AquaSwarm%20Waste%20Collection%20Research%281%29.png)

### Mechanism concept

1. Floating debris enters the front collection area.
2. Side guides help direct waste towards the mesh.
3. The mesh retains the collected material.
4. Water drains through the mesh.
5. The removable compartment can be taken out and emptied.

### Collection approaches considered

| Mechanism | Advantages | Limitations |
|---|---|---|
| Front-mounted mesh net | Simple, lightweight and removable | Limited capacity |
| Conveyor-based collection | Potential for continuous collection | More complex and power-intensive |
| Guided collection basket | Relatively simple construction | Depends on collection geometry |

The front-mounted mesh collector is the preliminary choice for V0.1 because of its simplicity and ease of fabrication.

---

## Camera and Live Monitoring

AquaSwarm is planned to include a forward-facing camera for monitoring the surroundings.

The camera feed will be transmitted to a browser-based dashboard through the Raspberry Pi.

![AquaSwarm V0.1 – Camera and Monitoring Research](assets/AquaSwarm%20V0.1%20Monitoring%20System%281%29.png)

### Proposed monitoring features

- Live camera feed.
- Connection status.
- Battery monitoring.
- System status information.
- Remote movement controls.

### Proposed video architecture

**Camera → Raspberry Pi 4 → Local Wi-Fi → Browser Dashboard**

Camera hardware and streaming performance will be evaluated during implementation.

Future versions may explore computer vision for identifying floating waste and other objects.

---

## Communication and Remote Control

The proposed primary communication method is local Wi-Fi.

This allows an operator to connect to the robot through a phone or laptop without requiring an external internet connection.

![AquaSwarm – Communication Blueprint](assets/AquaSwarm%20Communication%20Blueprint%281%29.png)

### Proposed communication architecture

| Technology | Purpose |
|---|---|
| Wi-Fi | Main operator communication |
| HTTP | Dashboard access and control requests |
| WebSocket | Live system updates |
| MJPEG over HTTP | Proposed video streaming |
| UART | Raspberry Pi–Arduino communication |
| JSON | Structured command and status data |

### Proposed dashboard

The browser-based dashboard is intended to provide:

- Forward, backward, left and right controls.
- Emergency-stop control.
- Camera feed.
- Speed control.
- Connection status.
- Battery and system information.

### Offline operation

AquaSwarm's basic remote-control system is designed to operate over a local Wi-Fi network.

An internet connection is not required for the proposed local control and monitoring functions.

### Safety considerations

The implementation should include:

- Emergency-stop functionality.
- Automatic motor stop after communication loss.
- Clear connection-status indicators.
- Validation of movement commands.
- Protected electronics and electrical connections.

---

## Power System

The power system must support both the computing electronics and propulsion components.

The preliminary architecture separates the electronics power path from the motor power path.

![AquaSwarm V0.1 – Power System Research](assets/AquaSwarm%20V0.1%20Power%20System%20Infographic%281%29.png)

### Proposed power distribution

**Rechargeable battery system → Power management → Separate regulated supply paths**

The electronics supply is intended for:

- Raspberry Pi 4.
- Arduino Uno.
- Camera module.
- Communication hardware.

The motor supply is intended for:

- Motor drivers or ESCs.
- Left propulsion motor.
- Right propulsion motor.

### Power-system considerations

- Voltage compatibility.
- Peak and continuous current requirements.
- Battery capacity and operating time.
- Regulated power for electronics.
- Battery protection.
- Charging compatibility.
- Emergency shutdown.
- Water-resistant electrical enclosures.

Exact battery specifications will be selected after the motors and other electrical loads are finalised.

---

## Operating Sequence

The intended V0.1 operating sequence is:

1. Power on the robot.
2. Connect the operator's phone or laptop to the local Wi-Fi network.
3. Open the browser-based control dashboard.
4. View the live camera feed.
5. Send movement commands.
6. Navigate towards accessible floating debris.
7. Collect waste using the front-mounted mesh mechanism.
8. Return and empty the collection compartment.

This describes the proposed workflow and will be validated during physical testing.

---

## Preliminary Bill of Materials

The following list identifies the major components expected to be required for the first prototype.

| Component | Quantity | Purpose |
|---|---:|---|
| Raspberry Pi 4 | 1 | Main processing |
| Arduino Uno | 1 | Motor control |
| Camera module | 1 | Live monitoring |
| DC motors / underwater thrusters | 2 | Propulsion |
| Motor drivers / ESCs | 2 or as required | Motor control |
| Protected rechargeable battery system | 1 | Power |
| Voltage regulators | As required | Power distribution |
| Wi-Fi hardware | 1 system | Communication |
| Floating hull structures | 2 | Buoyancy |
| Mesh collection material | 1 set | Waste collection |
| Electronics enclosure | 1 | Protection |
| Wiring and connectors | 1 set | Electrical connections |
| Mounting hardware | 1 set | Mechanical assembly |

**Note:** This is a preliminary Bill of Materials. Exact models, ratings and quantities remain subject to component selection and compatibility checks.

---

## Technical Feasibility

The initial research evaluated the major subsystems based on their implementation complexity and engineering requirements.

| Subsystem | Preliminary feasibility | Main challenge |
|---|---|---|
| Catamaran platform | High | Buoyancy and stability |
| Raspberry Pi processing | High | Power consumption and heat |
| Arduino motor control | High | Motor-driver compatibility |
| Camera monitoring | High | Video quality and latency |
| Wi-Fi communication | High | Range and reliability |
| Twin-motor propulsion | High | Thrust and power selection |
| Mesh collection system | High | Capacity and collection efficiency |
| Complete integration | Moderate | Coordinating all subsystems |

These are preliminary research assessments, not results from physical testing.

---

## Risk Analysis

Several engineering risks were identified during the feasibility stage.

| Risk | Potential impact | Proposed mitigation |
|---|---|---|
| Water entering enclosure | Electronics failure | Sealed enclosure and testing |
| Insufficient buoyancy | Platform instability | Displacement calculations |
| Battery depletion | Interrupted operation | Runtime estimation and monitoring |
| Motor overheating | Propulsion failure | Suitable motor ratings |
| Wi-Fi disconnection | Loss of control | Timeout and automatic motor stop |
| Collector overload | Reduced stability | Collection capacity limits |
| Camera interruption | Loss of visibility | Connection monitoring |

Safety, stability and waterproofing will be important priorities during prototype development.

---

## Estimated Budget

The preliminary estimated budget for AquaSwarm V0.1 is:

| Category | Estimated cost |
|---|---:|
| Raspberry Pi and Arduino | ₹5,000–7,000 |
| Camera system | ₹1,000–2,000 |
| Propulsion system | ₹2,000–4,000 |
| Battery and power management | ₹2,000–3,500 |
| Floating platform materials | ₹1,500–3,000 |
| Collection mechanism | ₹500–1,500 |
| Wiring, connectors and enclosure | ₹1,000–2,000 |
| Miscellaneous | Approximately ₹1,000 |

### Total preliminary estimate

**₹14,000–24,000**

This is an initial planning estimate, not a confirmed purchase quotation. Actual expenditure will depend on the final component choices and supplier prices.

---

## Development Roadmap

AquaSwarm is intended to develop progressively, with each version introducing additional capabilities.

| Version | Planned development |
|---|---|
| V0.1 | Basic floating platform, remote control and collection concept |
| V0.2 | Improved camera and monitoring |
| V0.3 | Additional sensor integration |
| V0.4 | AI-assisted waste detection |
| V0.5 | Improved collection mechanism |
| V1.0 | Initial autonomous navigation |
| V2–V4 | Mapping and advanced navigation |
| V5–V6 | Multi-robot coordination |
| V7–V8 | Advanced autonomous AquaSwarm ecosystem |

![AquaSwarm V0.1 – Development Roadmap](assets/AquaSwarm%20V0.1%20Technical%20Roadmap%281%29.png)

The roadmap represents the long-term development vision. These features have not yet been implemented.

---

## Future Vision – AquaSwarm V8

The long-term vision is to develop AquaSwarm into an intelligent fleet of autonomous aquatic cleanup robots.

![AquaSwarm V8 – Future Swarm Concept](assets/AquaSwarm%20V8%20Lake%20Cleanup%20Swarm%281%29.png)

Potential future capabilities include:

- AI-based floating-waste detection.
- Autonomous navigation using GPS and vision.
- Mapping of water-surface areas.
- Coordinated multi-robot operation.
- Automated waste collection and storage.
- Water-quality monitoring.
- Real-time fleet monitoring and analytics.
- Improved energy management.

AquaSwarm V8 is a conceptual long-term vision, not a description of the current V0.1 system.

---

## Current Project Status

<details>
<summary><strong>V0.1 – Concept and Technical Planning</strong></summary>

The initial research and planning phase has been completed.

The work includes:

- Defined project problem and objectives.
- Proposed system architecture.
- Controller architecture.
- Propulsion research.
- Floating platform and hull research.
- Waste collection mechanism research.
- Camera and monitoring research.
- Communication and remote-control research.
- Power-system research.
- Preliminary Bill of Materials.
- Technical feasibility assessment.
- Risk analysis.
- Preliminary budget.
- Future development roadmap.

</details>

**Current stage:** Concept Development and Technical Planning.

**Next stage:** Hardware selection, software development, mechanical construction and controlled testing.

## Final Project Overview

![AquaSwarm V0.1 – Final Technical Overview](assets/AquaSwarm%20V0.1%20Technical%20Overview%281%29.png)

AquaSwarm V0.1 establishes the initial technical foundation for a robotic water-surface cleanup platform.

The project brings together robotics, embedded systems, wireless communication, mechanical design and environmental problem-solving.

The immediate goal is to move from research and planning towards a functional prototype, validate its core systems and gradually introduce more advanced capabilities.

> **Cleaner Water. A Greener Future.**

---

## Acknowledgements

Developed as part of **Hack Club Half Life**.

Thank you to Hack Club for providing the opportunity to explore, research and develop an engineering project around a real-world environmental challenge.

**Project:** AquaSwarm  
**Version:** V0.1  
**Development phase:** Initial research and technical planning  
**Status:** Concept documentation completed; prototype development pending

---

*Small robots. Cleaner lakes. A brighter future.*
