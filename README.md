# AmpAware - Smart Plug Base 🔌⚡

<img src="Product.jpg" alt="Product Image" width="400" height="400">

## Engineering Design Project - Semester 2

### 👥 Team: Wired Wizards
<img src="Team.jpg" alt="Team Image" width="400" height="300">

#### Contributors:
- **Ransika L.G.C.** - Coding & IoT Integration
- **Basith M.N.A.** -  Enclosure Design
- **Kumarage R.V.** -  PCB design & Testing
- **Samuditha H.K.P.** - Firmware Development & System Architecture


## 📂 Project Repository Structure

```
AmpAware/
│
├── 📁 docs/                          # 📋 Project Documentation
│   ├── Design_report.pdf             # Detailed design documentation
│   ├── final_onesilde_pitch_wiredwizards.pdf  # Project pitch presentation
│   └── Wired_wizards_EDP_proposal.pdf # Initial project proposal
│
├── 📁 src/                           # 💻 Source Code
│   └── controlling.ino               # ESP32 firmware (Blynk integration)
│
├── 📁 Schematics & PCB/              # ⚡ Hardware Design Files
│   ├── ESP32-WROOM-32.IntLib         # Component library
│   └── Esp32.SchDoc                  # Schematic design
│
├── 📁 MCU datasheet/                 # 📊 Technical References  
│   ├── esp-wroom-32_datasheet.pdf    # ESP32 specifications
│   └── mcu/                          # Additional MCU documentation
│
├── 🖼️ Product.jpg                    # Product demonstration image
├── 🖼️ Team.jpg                       # Team photo
├── 📄 README.md                      # Project overview (this file)
├── 📄 LICENSE                        # Open-source license
└── 📄 .gitignore                     # Git configuration
```


---

## 🎯 Project Overview

**AmpAware Smart Plug Base** is an innovative IoT-enabled smart plug solution designed to revolutionize energy management in modern households. This intelligent device bridges the gap between traditional electrical appliances and smart home automation, offering:

- **🏠 Smart Home Integration** - Seamless control via Blynk IoT platform
- **⚡ Real-time Energy Monitoring** - Track power consumption instantly
- **🛡️ Advanced Safety Features** - Surge protection and overcurrent safety
- **📱 Remote Control** - Manage appliances from anywhere in the world
- **💰 Cost-Effective Solution** - Smart functionality without full home automation investment

### 🚀 Why AmpAware?

Unlike expensive smart home systems that require complete infrastructure overhaul, **AmpAware** provides targeted smart control for individual appliances. This makes smart home technology accessible, affordable, and practical for everyday users who want to optimize energy consumption and enhance convenience.

---

## 📋 Problem Statement & Market Need

### 🔍 Identified Challenges:
| Problem | Impact | AmpAware Solution |
|---------|---------|-------------------|
| **Forgotten Appliances** | Energy waste, fire hazards | Remote monitoring & control |
| **No Energy Visibility** | High electricity bills | Real-time power consumption tracking |
| **Limited Appliance Control** | Inconvenience, inefficiency | Smart scheduling & automation |
| **Expensive Smart Home Systems** | High barrier to entry | Cost-effective individual device control |

### 🎯 Target Market:
- **Tech-savvy households** seeking smart home entry point
- **Energy-conscious consumers** wanting to reduce electricity costs
- **Busy professionals** needing remote appliance control
- **Safety-focused users** requiring surge protection

---

## ✨ Features & Specifications

### 🌟 Key Features:
```
🔄 Remote Control        │ Turn devices on/off via Blynk IoT app
🔲 Manual Control        │ Physical button for direct switching  
📊 Power Monitoring      │ Real-time voltage and current measurement
🛡️ Safety Protection     │ Surge & overcurrent protection systems
📱 Mobile Integration    │ Seamless Blynk IoT app connectivity
🔧 Easy Installation     │ Standard plug socket compatibility
💡 Status Indicators     │ LED feedback for device status
🌐 Wi-Fi Connectivity    │ 2.4GHz wireless communication
```

### 📐 Technical Specifications:

#### ⚡ Electrical Ratings:
- **Input Voltage**: 100-240V AC (Universal compatibility)
- **Maximum Load**: 13A (3120W at 240V)
- **Frequency**: 50/60Hz
- **Safety Standard**: Built-in surge protection

#### 🔗 Connectivity:
- **Wi-Fi Standard**: 802.11b/g/n (2.4GHz-2.5GHz)
- **IoT Platform**: Blynk Cloud Integration
- **Communication Range**: 30+ meters indoors
- **Network Security**: WPA2/WPA3 encryption support

#### 🖥️ Hardware Core:
- **Microcontroller**: ESP32 WROOM-32D (Dual-core 240MHz)
- **Memory**: 4MB Flash, 520KB SRAM
- **Current Sensor**: ACS712 (30A) - ±1% accuracy
- **Voltage Sensor**: ZMPT101B (230V) - High precision AC voltage detection
- **Relay**: 5V DC Controlled, 13A AC switching capacity

#### 🏠 Physical Design:
- **Operating Temperature**: 0°C to 40°C
- **Enclosure Material**: Heat-resistant PLA (Prototype), Industrial polymer (Production)
- **Form Factor**: Standard 13A plug socket size
- **Dimensions**: 85mm x 55mm x 45mm (L x W x H)
- **Weight**: 120g (lightweight design)

#### 📱 Software Features:
- **OTA Updates**: Over-the-air firmware updates
- **Real-time Monitoring**: Live power consumption data
- **Remote Diagnostics**: System health monitoring
- **Scheduling**: Automated on/off timers
- **Energy Reports**: Historical usage analytics

---

## 🏗️ System Architecture

### 📊 Block Diagram Overview:
```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   AC Input      │    │   ESP32 MCU     │    │   Mobile App    │
│   (230V)        │───▶│   Controller    │◄──▶│   (Blynk IoT)   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│  Relay Control  │    │   Sensors       │    │   Wi-Fi         │
│  & Protection   │    │   (ACS712/      │    │   Communication │
│                 │    │    ZMPT101B)    │    │   Module        │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### 🔧 Hardware Components:

#### 🔌 Power Management System:
- **AC Input (230V)**: Standard household power supply
- **Relay Module (5V)**: High-capacity switching for connected devices
- **Surge Protection Circuit**: Fuse-based safety system
- **Power Supply Unit**: Converts AC to DC for MCU operation

#### 🧠 Control & Processing Unit:
- **ESP32 WROOM-32D**: 
  - Dual-core processor for multitasking
  - Built-in Wi-Fi and Bluetooth capabilities
  - 4MB Flash memory for firmware storage
  - GPIO pins for sensor and actuator control

#### 📡 Communication Module:
- **Wi-Fi (2.4GHz)**: Primary connectivity for IoT operations
- **Blynk Protocol**: Secure cloud communication
- **OTA Support**: Remote firmware update capability
- **Local Network Integration**: LAN-based control backup

#### 📊 Sensing & Monitoring:
- **ACS712 Current Sensor (30A)**:
  - Hall-effect based current measurement
  - Real-time power consumption calculation
  - Overcurrent detection and protection
  
- **ZMPT101B Voltage Sensor (230V)**:
  - Precise AC voltage monitoring
  - Supply voltage quality assessment
  - Under/over-voltage protection

#### 👤 User Interface Elements:
- **Physical Push Button**: Manual on/off control with debouncing
- **Status LED Indicator**: Visual feedback for device state
- **Mobile App (Blynk IoT)**: 
  - Real-time control and monitoring
  - Energy consumption graphs
  - Scheduling and automation features
  - Remote access from anywhere

#### 🏠 Mechanical Design:
- **Compact Enclosure**: Standard 13A plug form factor
- **Modular Assembly**: Easy maintenance and component replacement
- **Heat Dissipation**: Ventilation design for thermal management
- **Safety Compliance**: Electrical safety standards adherence

---

## 🚀 Getting Started

### 📦 Installation Process:
1. **📱 Download Blynk App** - Install from App Store/Google Play
2. **🔌 Physical Setup** - Insert AmpAware into wall socket
3. **⚡ Connect Device** - Plug your appliance into AmpAware
4. **🌐 Wi-Fi Configuration** - Connect device to your home network
5. **📊 App Setup** - Configure Blynk dashboard and controls
6. **✅ Test & Monitor** - Verify remote control and monitoring functions

### 📱 Blynk App Configuration:
```
Virtual Pins Configuration:
├── V12: Relay Control Button
├── V1:  Voltage Reading Display
├── V2:  Current Reading Display  
├── V3:  Power Consumption Display
└── V4:  Device Status Indicator
```

### 🛠️ Quick Setup Guide:
1. **Power On**: LED indicator will show connection status
2. **Wi-Fi Setup**: Device creates hotspot for initial configuration
3. **Blynk Connection**: Enter authentication token from app
4. **Device Pairing**: Scan QR code or enter device ID
5. **Ready to Use**: Control remotely via smartphone

---

## 💻 Firmware Architecture

### 📁 Code Structure:
```cpp
Main Components:
├── Blynk Integration     → Remote control via mobile app
├── Physical Button       → Manual on/off control with debouncing  
├── Relay Control         → Device switching mechanism
├── LED Status Indicator  → Visual feedback system
├── OTA Updates          → Over-the-air firmware updates
├── Wi-Fi Management     → Network connectivity handling
└── Safety Monitoring    → Overcurrent and surge protection
```

### 🔧 Key Functions:
- **`BLYNK_WRITE(V12)`**: Handles remote control commands
- **`checkPhysicalButton()`**: Monitors manual button presses
- **`BLYNK_CONNECTED()`**: Synchronizes device state on connection
- **`ArduinoOTA.handle()`**: Enables remote firmware updates

## Project Repository Structure
```
AmpAware/
│── docs/             # Reports & Documentation
│── hardware/         # PCB designs, Schematics, Enclosure files
│── firmware/         # ESP32 Firmware & Code
│── mobile_app/       # App configurations (if applicable)
│── tests/            # Testing results & scripts
│── images/           # Photos & Diagrams
│── README.md         # Project overview (this file)
│── LICENSE           # Open-source license
│── .gitignore        # Git ignored files
```

## 🔮 Future Enhancements & Roadmap

### 🎯 Phase 1: Enhanced Connectivity
- **🏠 Smart Home Integration**: 
  - Amazon Alexa compatibility
  - Google Assistant voice control
  - Apple HomeKit integration
- **🔗 Alternative Protocols**: 
  - Zigbee support for mesh networking
  - Z-Wave compatibility for better range
  - Matter protocol for universal compatibility

### 🎯 Phase 2: AI & Automation
- **🤖 Machine Learning Features**:
  - Predictive device control based on usage patterns
  - AI-powered energy optimization recommendations
  - Anomaly detection for unusual power consumption
- **📅 Advanced Scheduling**:
  - Smart scheduling based on electricity tariffs
  - Seasonal automation adjustments
  - Integration with weather data for adaptive control

### 🎯 Phase 3: Product Variants
- **🌍 Global Market Adaptation**:
  - Multiple plug standards (US, EU, UK, AU)
  - Different voltage ratings (110V, 230V, 240V)
  - Frequency adaptations (50Hz/60Hz)
- **⚡ Enhanced Features**:
  - Integrated USB charging ports (USB-A, USB-C)
  - Power bank functionality for backup
  - Solar panel integration compatibility

### 🎯 Phase 4: Commercial Features
- **🏢 Industrial Applications**:
  - Higher current ratings (20A, 30A)
  - Industrial protocol support (Modbus, BACnet)
  - Enterprise management dashboard
- **📊 Advanced Analytics**:
  - Cloud-based energy analytics
  - Cost optimization algorithms
  - Carbon footprint tracking

---

## 🔗 Resources & Links

### 📚 Documentation:
- **📋 Project Presentation**: [Canva Design](https://www.canva.com/design/DAGOxdHLGcY/C9ncWn3HoFnEbKjtEisTJQ/view?utm_content=DAGOxdHLGcY&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hfe9ea47371)

### 🛠️ Development Tools:
- **Arduino IDE**: For firmware development and uploading
- **Blynk App**: For mobile interface and IoT connectivity
- **Altium Designer**: For PCB design and schematic capture
- **Fusion 360**: For 3D modeling and enclosure design

---

## 📞 Contact & Support

### 👥 Team: Wired Wizards
**Project Type**: Engineering Design Project - Semester 2  
**Institution**: Electronic & Telecommunication Engineering, University of Moratuwa, Sri Lanka  
**Course**: Electronic Design Project (Semester 2) 

### 📧 Get in Touch:
For technical questions, collaboration opportunities, or project inquiries, please reach out to any team member through the university email system.

### 🤝 Contributing:
We welcome contributions to improve AmpAware! Please feel free to:
- 🐛 Report bugs and issues
- 💡 Suggest new features
- 📖 Improve documentation
- 🔧 Submit pull requests

---

## 📄 License

This project is open-source and available under the [LICENSE](LICENSE) terms. Feel free to use, modify, and distribute according to the license specifications.

---

**⚡ AmpAware - Making Smart Energy Management Accessible to Everyone! ⚡**


