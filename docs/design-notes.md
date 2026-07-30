# Recovered STORM design notes

These notes are a cleaned summary of an older requirements file. Values below are **design targets or alternatives**, not completed test results.

## Mission and packaging goals

* Package the primary electronics, telemetry, and batteries in an approximately 100 mm diameter by 50 mm cylindrical volume.
* Allow a second volume for recovery hardware if the parachute could not be packaged internally.
* Keep the primary module near an early 500 g allocation.
* Use modular payload sections so research sensors and cameras could be added without redesigning the core computer.

## Energy storage

Candidate single-cell configurations included:

|Candidate|Nominal recovered estimate|Design rationale|
|-|-:|-|
|3 x 21700 cells|15 Ah / 54 Wh|Higher capacity and thermal mass; fewer heater zones|
|3 x 18650 cells|10.5 Ah|Available cells and convenient single-layer packaging|
|2 x 7060100 pouch cells|12 Ah|Flat stacked packaging|

The recovered planning target was approximately 10 W continuous system power. The battery system was to remain 1S to simplify onboard charging.

## Thermal management

* Wrap cells with resistive flex-PCB heaters.
* Monitor temperatures around the mainboard and inside the battery pack.
* Control heating through the flight computer rather than a permanently active circuit.
* Investigate reflective barriers and low-density insulation.
* Model heat transfer in a low-pressure enclosed volume, where convection differs from ground conditions.
* Retain local board heaters and controllable fans as implementation options.

## Charging and solar input

* Support charging while the main compute system is off.
* Use USB-C for ground charging and programming.
* Reuse the onboard charging path for a solar input where practical.
* Evaluate flexible solar cells around the cylindrical body versus simpler linear cells.

## Power-state behavior

The desired behavior resembled a phone rather than a hard battery disconnect:

* the charging/system controller remains connected to the cell;
* a guarded button or switch requests startup;
* the supervisory rail enables first;
* software enables expensive subsystems only when required; and
* the system can return to a very low-power state without mechanically disconnecting the battery.

## Compute architecture

The recovered requirements deliberately separated two workloads:

### Supervisory processor

A comparatively powerful MCU would handle sensor readout, data storage, telemetry, system sequencing, and power/thermal management. Candidate families were compared on peripheral support, software-library maturity, core voltage, and availability.

### FPGA

The FPGA would handle camera/video timing, parallel interfaces, buffering, packet-oriented utilities, and selected high-reliability functions. Spartan-6 was attractive because it was inexpensive and existing development assets were available; newer families offered easier workflows at greater cost.

## Sensors

The sensor plan included:

* barometric pressure;
* temperature;
* three-axis acceleration;
* three-axis angular rate;
* magnetic heading;
* temperature sensing near each thermal zone; and
* a possible ring of light sensors to estimate sun direction and assess solar-panel orientation.

## Communications and imaging

### Cellular / GNSS

Requirements called for LTE Cat NB2 or better, GNSS support, a documented UART interface, and a module form factor that avoided a custom RF implementation.

### Long-range radio

The preferred telemetry solution was a 915 MHz or 2.4 GHz LoRa/mLRS-class link with up to 1 W module output. A 100 km line-of-sight figure appears in the recovered notes as a target only; it was not a demonstrated result.

### Imaging

An OV7670-class low-resolution camera was considered for live imagery through FPGA processing. The notes proposed roughly VGA-class capture and low-frame-rate transmission, while recognizing that the telemetry data rate would constrain the final method.

## Recovery and research payload concepts

* Investigate compact mortar-style parachute deployment.
* Keep a dedicated action camera or other research payload separate from the core flight-computer module.
* Treat recovery and research payloads as replaceable extensions rather than permanent mainboard functions.

## Items intentionally not presented as results

The original notes contain early choices, estimates, and open questions. This archive does not claim that the packaging mass, endurance, solar charging, thermal performance, radio range, image link, or recovery system was completed or verified.

