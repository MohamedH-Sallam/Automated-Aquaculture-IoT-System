# Hardware design

| Component | Role in the documented prototype | Notes from the report |
|:|:|:|
| Arduino UNO R3 | Main controller | Used for monitoring and control |
| pH probe and BNC module | Water acidity measurement | The probe was stored in 4.0 M KCl between readings |
| DS18B20 waterproof sensor | Water temperature measurement | Report states a range of minus 55 °C to 125 °C and reports accuracy as ±5 percent |
| Aquarium heater | Temperature actuation | Switched through a relay |
| 5 cm syringe and stepper motor | KOH dosing | Reported dose was 0.01 M KOH solution |
| Stepper motor and servo | Robotic crane movement | Vertical probe movement and horizontal positioning |
| HC 05 Bluetooth module | Controller to phone communication | Bluetooth serial link |
| L293D motor driver shield | Motor actuation | Listed for stepper, servo, and DC motor control |
| Three submersible pumps | Water transfer | Reported measured flow rate was 31.25 ± 2.66 mL/s at 7.5 V |
| Filter paper and activated carbon | Suspended solids treatment | 1.00 ± 0.01 g powdered activated carbon |
| Aquarium aerator | Aeration and mixing | Helped distribute heat and pH dosing |
| Servo driven feeder | Feed release | Custom dispenser for pellets and dried alfalfa |

## Main dimensions and solution values

* Main aquarium container: 21.0 ± 0.5 L in the materials list. The design description also gives 21 L ± 1 L.
* Secondary container: 10 ± 1 L.
* pH target: 7 to 8.
* Temperature target: 27 to 30 °C.
* Potassium hydroxide concentration: 0.01 M.
* Probe storage solution: 4.0 M potassium chloride.
* Activated carbon used in the filtration test: 1.00 ± 0.01 g.
* Reported syringe test dose: 3.15 ± 0.05 mL.

## Wiring evidence

![Original controller wiring diagram](../assets/arduino_wiring_diagram.png)

The diagram is extracted from the source report. It should be checked against the physical build before using it to reproduce the circuit.
