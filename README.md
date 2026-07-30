# Summary
This is an archive for project STORM, a modular flight computer designed by myself on behalf of ANU Rocketry Payoload Team, between late 2024 and early 2025. 
It features a spartan 6 FPGA, STM32F405 MCU and assorted peripherals, namely a Quectel cellular and gps module, MLRS 915mhz transponder for telemetry, Omnivision low-resolution camera for snapshot image transmission, USB-C for charging, solar cell connection, a large 18650 based battery pack featuring flex-pcb resistive heaters, multiple fan connections for thermal regulation, usb programming, redundant storage via micro-sd, onboard barometer, QOL features like expansive GPIO, JTAG breakouts, QWIIC connectors, assorted status leds. 
The design was optimized over several iterations to reduce cost, three major iterations occured. The final iteration swapped from BGA to QFP for the spartan 6 and cut several components. Final cost was $250 AUD for 2pcs assembled via JLCPCB.

# Documentation index

|Document|Purpose|Revision caveat|
|-|-|-|
|[MONAD project-specific extract (PDF)](MONAD-project-extract.pdf)|Useful PDF pages with overview, preliminary limits, pin tables, bus addresses, GPIO, and radio commands|Primarily reflects the earlier BGA/external-RAM board revision; values remain unverified|
|[Architecture](architecture.md)|Concise description of compute domains, buses, power, telemetry, and interfaces|System-level summary, not a manufacturing specification|
|[Recovered design notes](design-notes.md)|Cleaned requirements, alternatives, and targets from the original planning notes|Targets are not represented as achieved results|
|[Document archive](archive/README.md)|Full 85-page export and repaired DOCX source|Most content is copied component-reference material and is retained only for provenance|

## Statement of work
With the exception of some requirement documentation, This is entirely my own work, all PCB design, CAD, etc was my own work. 
