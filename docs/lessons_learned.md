# Engineering lessons

## Motor thermal management

The syringe pump stepper motor overheated when current was continuously applied to hold position. The report records the use of the motor library release function to stop supplying current while the motor was idle.

## Actuator sizing

A low torque, high speed DC motor could not lift the pH probe reliably. The team replaced it with a stepper motor for the vertical motion mechanism.

## Heater handling

The glass heater broke after being removed from water while it was operating. This illustrates the need to respect immersion requirements and thermal shock limitations.

## Water mixing

The temperature test took longer without the aerator. The report attributes this to poor heat distribution and notes that aeration also helped distribute pH dosing.

## Chemical selection

Sodium bicarbonate was tried before potassium hydroxide. The report found that the sodium bicarbonate used was too weak for the intended pH adjustment, so the team changed to 0.01 M KOH solution.

## Extension priorities from the report

* Add a DS3231 real time clock to preserve scheduled operations across power loss.
* Improve treatment for additional water quality parameters, especially ammonia removal.
* Expand the available control pins or revise the controller architecture before adding more actuators.
* Consider species specific presets for pH and temperature in the mobile application.

The final two points are future recommendations in the source report, not implemented capabilities.
