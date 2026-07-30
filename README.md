# Summary
This is an archive for project STORM, a modular flight computer designed by myself on behalf of ANU Rocketry Payload Team, between late 2024 and early 2025. 
The design consists of the MONAD mainboard, within the STORM system. 
It features a Spartan 6 FPGA, STM32F405 MCU and assorted peripherals, namely a Quectel cellular and GPS module, MLRS 915MHz transponder for telemetry, Omnivision low-resolution camera for snapshot image transmission, USB-C for charging, solar cell connection, a large 18650 based battery pack featuring flex-PCB resistive heaters, multiple fan connections for thermal regulation, USB programming, redundant storage via micro-SD, onboard barometer, QOL features like expansive GPIO, JTAG breakouts, QWIIC connectors, and assorted status LEDs. 

The design was optimized over several iterations to reduce cost; three major iterations occurred. The final iteration swapped from BGA to QFP for the Spartan 6 and cut several components. Final cost was $250 AUD for 2pcs assembled via JLCPCB.

## Visual Overview & Diagrams

**MONAD Hero 3D Render**  
A 3D render showcasing the assembled MONAD mainboard.  
[![MONAD Hero 3D Render](https://raw.githubusercontent.com/HecmacGPD/STORM/main/assets/images/monad-hero-3d.png)](https://github.com/HecmacGPD/STORM/blob/main/assets/images/monad-hero-3d.png)

**Assembly Concept**  
Last known render of the STORM assembly, Final design used watercut aluminium to form a base plate and a 3d printed chassis to optimize airflow via ducting.  
[![MONAD Current Assembly Concept](https://raw.githubusercontent.com/HecmacGPD/STORM/main/assets/images/monad-current-assembly-concept.png)](https://github.com/HecmacGPD/STORM/blob/main/assets/images/monad-current-assembly-concept.png)

**System Block Diagram**  
A high-level block diagram detailing the architecture, buses, and interconnects between the FPGA, MCU, and peripherals.  
[![MONAD System Block Diagram](https://raw.githubusercontent.com/HecmacGPD/STORM/main/assets/diagrams/monad-system-block-diagram.png)](https://github.com/HecmacGPD/STORM/blob/main/assets/diagrams/monad-system-block-diagram.png)

**Power-On Sequence**  
A timing and logic diagram illustrating the expected power-on sequence and startup logic.  
[![MONAD Power-On Sequence](https://raw.githubusercontent.com/HecmacGPD/STORM/main/assets/diagrams/monad-power-on-sequence.png)](https://github.com/HecmacGPD/STORM/blob/main/assets/diagrams/monad-power-on-sequence.png)

# Documentation Index

| Document | Purpose | Revision caveat |
|---|---|---|
| [MONAD project-specific extract (PDF)](https://github.com/HecmacGPD/STORM/blob/main/docs/MONAD-project-extract.pdf) | Useful PDF pages with overview, preliminary limits, pin tables, bus addresses, GPIO, and radio commands | Primarily reflects the earlier BGA/external-RAM board revision; values remain unverified |
| [Architecture](https://github.com/HecmacGPD/STORM/blob/main/docs/architecture.md) | Concise description of compute domains, buses, power, telemetry, and interfaces | System-level summary, not a manufacturing specification |
| [Recovered design notes](https://github.com/HecmacGPD/STORM/blob/main/docs/design-notes.md) | Cleaned requirements, alternatives, and targets from the original planning notes | Targets are not represented as achieved results |

## Statement of Work
With the exception of some requirement documentation, this is entirely my own work. All PCB design, CAD, etc., was my own work.
