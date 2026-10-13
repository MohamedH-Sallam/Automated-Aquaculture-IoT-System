# Control logic

This document translates the prose description in the source report into a readable functional sequence. It is not the original Arduino program.

## pH regulation

1. Move the pH probe from its 4.0 M KCl storage container into the aquarium.
2. Read the pH through the probe interface.
3. Compare the reading with the intended pH range of 7 to 8.
4. If pH requires an increase, operate the stepper driven syringe pump to dispense the KOH solution.
5. Use the aerator to help distribute the solution through the water.
6. Return the probe to its storage solution after measurement.
7. Release stepper motor current when the motor is idle, as recommended after the overheating issue recorded in the report.

## Temperature regulation

1. Read the DS18B20 water temperature.
2. Compare the measurement with the target range of 27 to 30 °C.
3. Switch the aquarium heater through its relay when heating is needed.
4. Keep aeration operating to improve mixing and heat distribution.
5. Continue measurement and feedback until the water approaches the target range.

The source report does not provide a complete software state machine, sampling interval, hysteresis values, timeout strategy, or fault handling logic. These details are therefore not asserted here.

## Water treatment and replacement

The described arrangement transfers water from the tank through filter paper and powdered activated carbon, then returns treated water for reuse. The report also describes external clean water addition. The design target was to reuse 25 percent of changed water and keep the TSS concentration below 100 mg/L.

## Feeding

A servo rotates a custom dispenser to release a selected feed compartment. The report describes pellets and dried alfalfa as separate feed types. A DS3231 real time clock was recommended for dependable schedule retention after power loss, but was not included in the documented prototype.
