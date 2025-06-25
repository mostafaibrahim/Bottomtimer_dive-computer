# 🌊 Community-Driven Dive Computer

[![Status: Beta Testing](https://img.shields.io/badge/Status-Beta%20Testing-orange.svg)]()
[![Community: Growing](https://img.shields.io/badge/Community-Growing-green.svg)]()
[![Made by Divers](https://img.shields.io/badge/Made%20by-Divers-blue.svg)]()
[![Safety First](https://img.shields.io/badge/Safety-First-red.svg)]()

> **Professional dive computer technology at an unbeatable price point**

An advanced dive computer featuring Bühlmann ZH-L16C decompression algorithms, dual sensor redundancy, and multiple diving modes - all at a fraction of traditional costs.

![Dive Computer Hero Image](./images/hero-image.jpg)

---

## 📋 Table of Contents

- [Features](#-features)
- [Product Gallery](#-product-gallery)
- [Technical Specifications](#-technical-specifications)
- [Beta Testing Program](#-beta-testing-program)
- [Getting Started](#-getting-started)
- [Hardware Overview](#-hardware-overview)
- [Software Architecture](#-software-architecture)
- [Safety & Compliance](#-safety--compliance)
- [Community](#-community)
- [Support](#-support)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)

---

## ✨ Features

### 🎯 **Core Functionality**
- **Bühlmann ZH-L16C Algorithm** with gradient factors for safe decompression
- **Dual Sensor System** (MS5837) for redundancy and button input
- **Multiple Display Modes** - Detailed view and Bottom Timer
- **Nitrox Support** - 21% to 40% oxygen mixtures
- **Real-time NDL/Deco** calculations with stop planning
- **Surface Interval Tracking** with tissue saturation monitoring

### 🔧 **Professional Features**
- **Bottom Timer Mode** - Perfect for technical divers using custom planning
- **Tissue Loading Visualization** - Real-time compartment monitoring
- **Decompression Planning** - Detailed ascent profiles with stop times
- **Dive Logging** - Comprehensive profile storage and analysis
- **Gas Mix Display** - Clear oxygen percentage indication
- **Battery Management** - Long-life rechargeable with charging indication

### 🎨 **User Experience**
- **High-Contrast Display** - Clear visibility in all conditions
- **Intuitive Interface** - Pressure-sensitive button system
- **Robust Construction** - Designed for demanding diving environments
- **Lightweight Design** - Comfortable for extended use

---

## 📸 Product Gallery

| Device Overview | Display Detail | Underwater Ready |
|:---:|:---:|:---:|
| ![Device Photo](./images/device-overview.jpg) | ![Display Photo](./images/display-detail.jpg) | ![Sealed Photo](./images/waterproof-design.jpg) |
| *Compact, rugged design* | *Crystal clear display* | *Pressure tested to 100m+* |

| Interface Demo | Algorithm Visualization | Bottom Timer Mode |
|:---:|:---:|:---:|
| ![Interface](./images/interface-demo.jpg) | ![Algorithm](./images/tissue-display.jpg) | ![Bottom Timer](./images/bottom-timer.jpg) |
| *Intuitive menu system* | *Real-time tissue loading* | *Clean bottom timer layout* |

---

## 🔧 Technical Specifications

### Hardware
| Component | Specification |
|-----------|---------------|
| **Microcontroller** | Raspberry Pi Pico (RP2040) |
| **Depth Sensors** | Dual MS5837-30BA pressure sensors |
| **Display** | ILI9341 TFT LCD (320x240, landscape) |
| **Battery** | Rechargeable Li-ion with USB-C charging |
| **Depth Rating** | 100+ meters (tested) |
| **Operating Temp** | -10°C to +50°C |
| **Case Material** | Marine-grade aluminum/polymer |
| **Weight** | ~150g (including battery) |

### Software
| Feature | Details |
|---------|---------|
| **Algorithm** | Bühlmann ZH-L16C (reduced 7-compartment model) |
| **Gradient Factors** | GF Low: 30%, GF High: 90% (optimized) |
| **Gas Support** | Air and Nitrox (21-40% O₂) |
| **Display Modes** | Detailed dive computer, Bottom timer |
| **Data Logging** | Full dive profile with 1-second resolution |
| **Safety Features** | Conservative factors, dual sensor validation |
| **Updates** | USB firmware updates |

---

## 🧪 Beta Testing Program

We're seeking experienced diving professionals to evaluate our dive computer in real-world conditions.

### 🎖️ **Ideal Beta Testers**
- **Dive Instructors** and **Dive Masters**
- **Technical Divers** and **Advanced Recreational Divers** 
- **Underwater Professionals** and **Scientific Divers**
- Active divers with **50+ dives annually**
- Experience with **multiple dive computer brands**

### 📦 **What's Included**
- Pre-production dive computer unit
- USB charging cable and documentation
- Direct developer communication channel
- Firmware updates throughout testing period
- Detailed feedback forms and reporting tools

### 📝 **Testing Requirements**
- Minimum **20 dives** over 3-month period
- **Detailed feedback** on usability and reliability
- **Comparison testing** with existing dive computer
- **Safety protocols** - use alongside primary computer
- **Written evaluation** at program completion

### 🎁 **Beta Tester Benefits**
- **Significant discount** on final production unit
- **Priority access** to future products and updates
- **Recognition** in community and documentation
- **Input** into final product features and design
- **Exclusive access** to beta tester community forum

---

## 🚀 Getting Started

### Prerequisites
- Basic understanding of decompression theory
- Valid diving certification (Open Water minimum)
- Access to regular diving opportunities
- Willingness to provide detailed feedback

### Beta Application Process

1. **Submit Application**
   ```
   Email: beta@divecomputer-project.com
   Subject: Beta Tester Application - [Your Name]
   
   Include:
   - Diving certifications and experience
   - Current dive computer(s) used
   - Typical diving activities and locations
   - Previous product testing experience
   - Contact information and availability
   ```

2. **Evaluation & Selection**
   - Application review (1-2 weeks)
   - Brief phone/video interview
   - Selection notification
   - Beta agreement and shipping details

3. **Testing Period**
   - 3-month evaluation period
   - Regular check-ins and feedback sessions
   - Firmware updates as available
   - Final evaluation report

---

## 🔨 Hardware Overview

### System Architecture
```
┌─────────────────┐    ┌─────────────────┐
│   Sensor 1      │    │   Sensor 2      │
│   (MS5837)      │    │   (MS5837)      │
│   I2C0          │    │   I2C1          │
└─────────┬───────┘    └─────────┬───────┘
          │                      │
          └──────────┬───────────┘
                     │
        ┌─────────────┴─────────────┐
        │     RP2040 Controller     │
        │   - Dual I2C interfaces   │
        │   - SPI for display       │
        │   - Algorithm processing  │
        └─────────────┬─────────────┘
                     │
        ┌─────────────┴─────────────┐
        │    ILI9341 Display        │
        │   - 320x240 resolution    │
        │   - High contrast LCD     │
        │   - Backlight control     │
        └───────────────────────────┘
```

### Sensor Configuration
- **Primary Depth Sensing**: Both sensors averaged for accuracy
- **Button Interface**: Pressure differential detection
- **Redundancy**: Automatic failover if one sensor fails
- **Calibration**: Real-time offset compensation

---

## 💻 Software Architecture

### Core Components

```python
# Main application modules
├── main.py                 # Primary dive computer logic
├── sensor_thread.py        # Dual sensor management
├── buhlmann_calculator.py  # Decompression algorithms
├── display_driver.py       # ILI9341 display interface
├── menu_system.py          # User interface management
└── safety_systems.py      # Redundancy and error handling
```

### Key Classes
- **`BuhlmannCalculator`** - Tissue loading and decompression planning
- **`SensorThread`** - Dual sensor reading and button detection
- **`ILI9341`** - Display driver with optimized drawing
- **`MenuSystem`** - Navigation and mode management

### Safety Features
- **Dual sensor validation** - Cross-reference depth readings
- **Conservative algorithms** - Safety margins in calculations
- **Error handling** - Graceful degradation on sensor failure
- **Data validation** - Sanity checks on all calculations

---

## ⚠️ Safety & Compliance

### ⚡ **Important Safety Notice**

**This dive computer is currently in BETA TESTING phase:**
- ✅ **Use alongside your primary dive computer**
- ✅ **Follow established diving safety protocols**
- ✅ **Report any issues immediately**
- ❌ **Not yet certified for solo dive computer use**
- ❌ **Not approved for commercial diving operations**

### 🛡️ **Safety Protocols**
- Algorithms based on proven Bühlmann ZH-L16C model
- Conservative gradient factors for additional safety margin
- Dual sensor redundancy for reliability
- Extensive testing in controlled environments
- Continuous monitoring during beta phase

### 📋 **Compliance Status**
- **Development Phase**: Beta testing and validation
- **Standards Target**: CE marking preparation
- **Future Certification**: ISO 6425 dive computer standard
- **Quality System**: Implementation in progress

---

## 🤝 Community

### 💬 **Join the Discussion**
- **Beta Tester Forum**: [Exclusive access for testers]
- **Email Support**: support@divecomputer-project.com
- **Development Updates**: Watch this repository for releases
- **Community Feedback**: Issues and discussions welcome

### 🌟 **Ways to Contribute**
- **Beta Testing**: Apply for the evaluation program
- **Feedback**: Share diving experience and suggestions
- **Documentation**: Help improve user guides and tutorials
- **Testing**: Validate algorithms and safety features
- **Promotion**: Share with fellow diving professionals

### 🏆 **Recognition**
Beta testers and significant contributors will be recognized in:
- Product documentation and website
- Community hall of fame
- Special edition device engravings (future)
- Priority access to new products

---

## 📞 Support

### 🆘 **Emergency Support**
- **Critical Safety Issues**: Immediate response within 4 hours
- **Phone**: +1-XXX-XXX-XXXX (emergency hotline for beta testers)
- **Email**: emergency@divecomputer-project.com

### 📧 **General Support**
- **Beta Testing**: beta@divecomputer-project.com
- **Technical Issues**: support@divecomputer-project.com
- **Sales Inquiries**: info@divecomputer-project.com
- **Partnership**: partnerships@divecomputer-project.com

### 📚 **Documentation**
- **User Manual**: [Coming with beta units]
- **Technical Reference**: Available in `/docs` folder
- **FAQ**: See [FREQUENTLY_ASKED_QUESTIONS.md](./docs/FAQ.md)
- **Troubleshooting**: See [TROUBLESHOOTING.md](./docs/TROUBLESHOOTING.md)

---

## 🗺️ Roadmap

### 📅 **Current Phase: Beta Testing (Q4 2024)**
- [ ] Complete beta tester selection
- [ ] Distribute 50 beta units to evaluators
- [ ] Collect comprehensive field testing data
- [ ] Iterate on firmware based on feedback
- [ ] Finalize production design

### 🎯 **Phase 2: Limited Production (Q1 2025)**
- [ ] Production run of 500 units
- [ ] CE marking certification process
- [ ] Establish distribution channels
- [ ] Launch direct sales program
- [ ] Build community support infrastructure

### 🚀 **Phase 3: Market Launch (Q2 2025)**
- [ ] Full production capability
- [ ] International distribution
- [ ] Advanced feature development
- [ ] Mobile app development
- [ ] Community-driven feature requests

### 🔮 **Future Phases (2025+)**
- [ ] Multi-gas support expansion
- [ ] Advanced display options
- [ ] Wireless connectivity features
- [ ] Community development platform
- [ ] Educational partnerships

---

## 🤝 Contributing

### 🧪 **Current Opportunities**
While the core codebase is currently closed during beta testing, you can contribute by:

1. **Beta Testing Application**
   - Real-world diving evaluation
   - Detailed feedback and reports
   - Safety validation in various conditions

2. **Documentation Improvement**
   - User guide suggestions
   - FAQ contributions
   - Translation assistance (future)

3. **Community Building**
   - Share with diving professionals
   - Provide use case scenarios
   - Connect with diving organizations

### 📋 **Future Contribution Plans**
Post-beta phase opportunities will include:
- Algorithm validation and testing
- Feature development suggestions
- Hardware modification proposals
- Safety protocol enhancements

---

## 📄 License & Legal

- **Current Status**: Proprietary software in beta testing
- **Community Input**: Welcomed and valued for future development
- **Intellectual Property**: All rights reserved during development phase
- **Future Plans**: Community-friendly licensing under consideration

---

## 🙏 Acknowledgments

Special thanks to:
- **Beta Testing Community** - Brave divers testing our technology
- **Diving Safety Organizations** - Guidance on best practices
- **Technical Diving Community** - Algorithm validation and feedback
- **Open Source Projects** - Inspiration for community-driven development
- **Marine Technology Pioneers** - Standing on the shoulders of giants

---

## 📊 Project Stats

![GitHub last commit](https://img.shields.io/github/last-commit/your-username/dive-computer)
![GitHub issues](https://img.shields.io/github/issues/your-username/dive-computer)
![GitHub stars](https://img.shields.io/github/stars/your-username/dive-computer)
![GitHub forks](https://img.shields.io/github/forks/your-username/dive-computer)

---

*Dive safe, dive smart, dive with the future.* 🤿

[![Powered by Community](https://img.shields.io/badge/Powered%20by-Community-blue.svg)]()
[![Made for Divers](https://img.shields.io/badge/Made%20for-Divers-turquoise.svg)]()
[![Safety First](https://img.shields.io/badge/Safety-First-red.svg)]()

---

**Contact Information:**
- 📧 **General**: info@divecomputer-project.com
- 🧪 **Beta Testing**: beta@divecomputer-project.com
- 🆘 **Support**: support@divecomputer-project.com
- 🤝 **Partnerships**: partnerships@divecomputer-project.com
