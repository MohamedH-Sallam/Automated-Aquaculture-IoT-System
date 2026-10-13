# System architecture

## System boundary

The documented prototype is a 21 L class aquarium for Nile tilapia. An Arduino UNO R3 reads pH and temperature measurements, operates pumps and motors, and communicates with a Flutter mobile application through an HC 05 Bluetooth module.

![System architecture](../assets/system_architecture.svg)

## Measurement and actuation paths

### pH

The pH probe feeds its measurement through a BNC interface to the Arduino. When the measured pH is outside the intended range, a stepper driven syringe pump doses 0.01 M KOH solution. The pH probe is moved by a small robotic crane and returned to 4.0 M KCl storage solution between measurements to protect the probe reference system.

### Temperature

A waterproof DS18B20 sensor reports water temperature. The Arduino switches an aquarium heater through a relay to move the water toward the target range of 27 to 30 °C. The report found that aeration improved heat distribution.

### Water treatment

Three submersible pumps move water between the aquarium, the treatment arrangement, and the clean water container. The treatment arrangement uses filter paper and powdered activated carbon to reduce total suspended solids. The reported design target was to reuse 25 percent of the changed water while keeping TSS below 100 mg/L.

### Feeding

A servo rotates a custom dispenser to release either fish pellets or dried alfalfa. The report describes an 80 percent pellet and 20 percent dried alfalfa diet as a research basis for the feeding design.

### Monitoring

The Arduino exchanges serial data with an HC 05 Bluetooth module. The mobile interface was developed in Flutter. The report documents local Bluetooth monitoring, not cloud storage or internet based remote control.

## Implementation boundary

The diagram and descriptions are reconstructed from the project report. The complete firmware and mobile application source files are not included in that report, so the repository does not present reconstructed code as original source.
