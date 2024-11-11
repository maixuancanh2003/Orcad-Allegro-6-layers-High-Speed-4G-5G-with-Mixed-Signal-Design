# High-Speed 4G/5G PCB with Mixed-Signal Design (Orcad/Allegro v17.4)

This repository includes visual content, design concepts, and PCB layout information for a high-performance 4G/5G board developed using Orcad/Allegro v17.4. As part of an ongoing scientific research project, this design integrates advanced microcontroller and network module components, along with industrial-grade I/O and mixed-signal capability, to support complex communication needs in industrial environments. Final project evaluation and publication are scheduled for June 2025.

> **Note**: **Full design files and technical specifications will be uploaded after the successful evaluation and official publication of the research in a scientific journal.**

## Project Overview

### 6-Layer PCB Details
- **Layers**: 6 layers, including 2 power layers and 4 signal layers.
- **Components**: Over 500 components.
- **PCB Material**: High-quality FR-4 for durability, thermal resistance, and optimal performance in high-speed applications.
- **Layer Spacing**: Optimized layer spacing for reduced interference and signal integrity.
- **PCB Thickness**: 1.6mm to support multi-layer stability and heat dissipation.

### Mixed-Signal Design Analysis
This board features a sophisticated mixed-signal design, where both analog and digital signals coexist within the same PCB layout. This requires special considerations to ensure reliable performance, minimize cross-talk, and preserve signal integrity in both the analog and digital domains.

#### Key Considerations in Mixed-Signal Design:
- **Analog and Digital Separation**:
  - Physical separation between analog and digital circuitry minimizes interference. Analog and digital components are placed on separate areas of the board, often with dedicated ground planes to avoid interference.
  - High-speed digital signals and sensitive analog signals are routed away from each other to prevent noise coupling.

- **Grounding Strategy**:
  - **Dedicated Ground Planes**: Separate ground planes are designated for analog and digital circuits, with careful attention to grounding points to prevent ground loops.
  - **Star Grounding**: Common grounding points (star points) are used to connect analog and digital grounds in one place, reducing the chance of noise looping through different parts of the board.

- **Power Distribution**:
  - **Separate Power Rails**: Analog and digital components receive power from isolated rails to minimize the risk of digital noise contaminating the analog signals.
  - **Decoupling Capacitors**: Strategic placement of decoupling capacitors near analog components stabilizes power and filters noise from the power supply, maintaining clean analog signals.

- **Routing Techniques**:
  - **Controlled Impedance for High-Speed Signals**: High-speed digital lines are routed with controlled impedance to maintain signal integrity.
  - **Minimized Crosstalk**: Analog signals are routed in a way that minimizes proximity to noisy digital lines, reducing the likelihood of interference. This includes techniques like differential routing for balanced signal paths.

- **Shielding and Filtering**:
  - **Shielded Traces**: Sensitive analog traces are sometimes shielded with ground traces or ground planes on either side to prevent coupling from high-speed digital signals.
  - **Filtering Components**: Filters (e.g., RC filters) are included on analog lines to filter out any high-frequency noise that might be introduced from the digital domain.

- **Electromagnetic Compatibility (EMC)**:
  - Mixed-signal boards can suffer from electromagnetic interference due to the presence of both high-speed digital signals and sensitive analog signals. EMC design practices are used to reduce emissions and susceptibility, including shielding, filtering, and layout optimization.

## Key Features
- **High-Speed PCB Design**: Engineered for reliable high-speed data communication to support 4G/5G network requirements.
- **Industrial I/O (24V)**: Capable of interfacing with industrial equipment, supporting I/O levels of 24V for wider application compatibility.
- **Communication Protocols**:
  - **Modbus**: Facilitates communication in industrial automation environments.
  - **RS232 & RS485**: Supports standard serial communication for embedded systems.
  - **Ethernet**: Provides fast and stable Ethernet connectivity for network integration and data transfer.

## USB Support

The ESP32-S3 and STM32F407VET6 microcontrollers support USB 1.1 full-speed (12 Mbps) with OTG (On-The-Go) functionality, allowing them to act as either USB hosts or devices. Although the USB operates at USB 2.0 full-speed, it lacks high-speed support (480 Mbps). This limitation makes the microcontrollers ideal for applications such as:

- USB Mass Storage
- Human Interface Devices (HID)
- Virtual COM Ports
- General-purpose data communication at full-speed rates

> **Note**: The OTG functionality allows these microcontrollers to switch between host and device modes, providing flexibility for a wide range of USB-based applications, while maintaining a reliable full-speed data rate of 12 Mbps.


### Image Display

| View          | Image                                      |
|---------------|--------------------------------------------|
| Front Left    | ![Front Left](Image/FrontLeft.png)         |
| Block Diagram | ![Block Diagram](BlockDiagram/BlockDiagram.png) |
| Idea          | ![Idea](BlockDiagram/Idea.png)             |

### Related Documents
This project interfaces with several key components and modules, detailed below:

1. **Raspberry Pi 4**
   - A versatile single-board computer frequently used for embedded systems.
   - [Datasheet](https://www.raspberrypi.org/documentation/)

2. **STM32F4VET6**
   - A high-performance microcontroller from STMicroelectronics, part of the STM32 family.
   - [Datasheet](https://www.st.com/en/microcontrollers-microprocessors/stm32f4-series.html)

3. **STM32S3**
   - Part of the STM32 series, designed for advanced digital applications.
   - [Datasheet](https://www.st.com/en/microcontrollers-microprocessors/stm32g0-series.html)

4. **SIM7600G-H**
   - A 4G LTE module supporting global bands, suitable for IoT applications.
   - [Datasheet](https://www.simcom.com/product/SIM7600X-H.html)

5. **Quectel 5G Mini PCIe**
   - A powerful 5G-capable module in a Mini PCIe form factor, ideal for high-speed data applications.
   - [Datasheet](https://www.quectel.com/product/5g-redcap-rg255c-mini-pcie-series/)


## Contact

For any questions or additional support, feel free to reach out:

- **Name**: Mai Xuan Canh
- **University**: Ho Chi Minh City University of Technology (HCMUT)
- **Major**: Control and Automation Engineering
- **LinkedIn**: [Canh Mai's LinkedIn](https://www.linkedin.com/in/maixuancanh2003/)
- **Email**: canhmai.work@gmail.com

---
