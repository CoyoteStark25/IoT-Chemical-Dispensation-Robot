# IoT Chemical Dispensation Robot (Agribot)

A Mobile-Controlled Pesticide Spraying Robot for Nigerian Smallholder Farmers



## Banner Image

![Agribot Banner](docs/banner.png)



## 1. Overview

The IoT Chemical Dispensation Robot (Agribot) is a low-cost, WiFi-controlled pesticide spraying robot built specifically for Nigerian and African smallholder farmers. It improves safety by reducing direct exposure to harmful chemicals, enhances spraying efficiency through servo-controlled aiming, and provides remote operation via live video streaming.

The project integrates embedded systems, robotics, IoT, and mechanical design into an accessible and locally adaptable solution.



## 2. Problem Statement (African Context)

Smallholder farmers across Nigeria depend heavily on manual backpack spraying. This leads to:

* High pesticide inhalation risk
* Frequent skin exposure through leaks and splashes
* Long-term health effects including respiratory issues, neurological damage, and cancer
* Low PPE usage due to heat, discomfort, and cost
* Increasing insecurity in rural farming environments
* Widespread use of unregulated or banned agrochemicals

Commercial robotic spraying systems are too expensive, require high-end sensors or GPS, and are not designed for rugged rural African farms. There is a pressing need for a safe, affordable, and easy-to-maintain spraying robot for smallholder agriculture.



## 3. Solution Summary

Agribot allows farmers to spray crops from a safe distance (30–50 meters) using:

* A WiFi-based control dashboard (no internet required)
* Real-time video streaming via ESP32-CAM
* Directional movement control
* Two-axis pan/tilt nozzle aiming
* 12V diaphragm pump for spraying
* Auto-timer spray mode
* Battery-powered operation for off-grid farms

The system is built from widely available, low-cost electronics accessible in African markets.



## 4. Features

### Mechanical and Electrical

* Differential drive system with two 12V DC geared motors
* 3-liter pesticide reservoir
* 12V diaphragm pump
* MG996R high-torque pan/tilt servos
* 12V 7.2Ah battery (2–3 hours runtime)

### Control System

* ESP32-CAM for WiFi access point and video
* Arduino Nano for motors, pump, and servos
* Reliable serial communication protocol
* Soft-start / soft-stop PWM control for pump safety

### User Interface

* Custom-built control dashboard (HTML/CSS/JavaScript)
* Real-time video feed
* Direction controls
* Servo angle sliders
* Spray on/off with timer
* Latency and FPS display
* Keyboard support (arrow keys + S to toggle spray)



## 5. How It Works

### System Architecture
```
ESP32-CAM -> WiFi Access Point + Web Dashboard + Video Stream
             |
             V
Arduino Nano -> Motor Control, Servo Control, Pump Control
```

### Communication Protocol

* Motor: M[F/B/L/R/S]
* Servo: S[P/T][angle]
* Pump: P[T][1/0]
* Status/Ping: ??0

The ESP32 handles networking and the interface; the Arduino executes real-time movement and spraying.



## 6. Impact and Results

### Safety Improvements

* Keeps farmers away from chemical exposure
* Eliminates direct inhalation and skin contact
* Minimizes dependence on PPE

### Operational Improvements

* Controlled spray direction and angle
* More uniform coverage
* Live video enables precise targeting
* Works on farms without internet infrastructure

### Practicality for African Smallholders

* Affordable and easy to replicate
* Uses locally available replacement parts
* Designed for rugged, uneven rural terrain
* Repairable by local technicians



## 7. Technologies Used

**Hardware:**
ESP32-CAM, Arduino Nano, L298N motor driver, DC geared motors, MG996R servos, diaphragm pump, 12V battery.

**Software:**
Arduino IDE, FreeRTOS (ESP32 tasks), HTML/CSS/JavaScript dashboard, serial communication protocol, CAD modeling tools.



## 8. Future Improvements

* Semi-autonomous navigation
* Larger tires and stronger motors for better stability in rugged terrains (Improved traction system)
* LiDAR or ultrasonic obstacle detection
* GPS-based farm mapping
* Solar charging
* Automatic chemical mixing



## 9. Author

**Blessed Osezuwa Ariagbofo**  
Hardware/Software Product Manager | IoT Engineer  
Email: [bariagbofo@gmail.com](mailto:bariagbofo@gmail.com)  
Nigeria



## 10. License

Open-source for educational and research use.  
Commercial use requires permission.
