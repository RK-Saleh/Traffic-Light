# Traffic-Light

This project demonstrates a basic traffic light system using an Arduino. It cycles through red, yellow, and green lights with specific timing intervals, mimicking a real-world traffic light.

---

## Overview

The system includes:
- **Red Light**: Represents "Stop."
- **Yellow Light**: Represents "Prepare to Stop/Go."
- **Green Light**: Represents "Go."
- A timed cycle manages the light transitions, ensuring smooth operation.

### Workflow:
1. Red light turns ON for 3 seconds.
2. Yellow light turns ON for 1.5 seconds.
3. Green light turns ON for 3 seconds.
4. A special transition phase turns the yellow light ON and green light OFF for 1.5 seconds before the cycle restarts.

---

## Hardware Requirements

- 1 Arduino board
- 3 LEDs:
  - Red
  - Yellow
  - Green
- 3 resistors (220Ω or similar for LEDs)
- Connecting wires
- Breadboard

---

## Circuit Diagram

- **Red LED**: Connected to pin 2.
- **Yellow LED**: Connected to pin 4.
- **Green LED**: Connected to pin 7.

Ensure each LED is connected to the respective pin via a resistor and a shared ground connection.

---

## Code Explanation

### Pin Assignments
- `pin1`: Pin 2, controls the red LED.
- `pin2`: Pin 4, controls the yellow LED.
- `pin3`: Pin 7, controls the green LED.

### Setup
- Configures all LED pins as outputs.

### Loop
The `loop` function manages the traffic light cycle:
1. Uses the `controlPin` helper function to:
   - Turn on the red light for 3 seconds.
   - Turn on the yellow light for 1.5 seconds.
   - Turn on the green light for 3 seconds.
2. Implements a special phase where:
   - The yellow light turns ON, and the green light turns OFF for 1.5 seconds.
   - Ensures the yellow light is turned OFF after the delay.

### `controlPin` Function
A utility function to simplify LED control:
- Turns the specified LED ON.
- Delays for the specified duration.
- Turns the LED OFF after the delay.

---

## Timing

- **Red Light**: 3 seconds.
- **Yellow Light**: 1.5 seconds.
- **Green Light**: 3 seconds.
- **Special Transition Phase**: Yellow light ON and green light OFF for 1.5 seconds.

---

## How to Use

1. Build the circuit as described above.
2. Upload the provided code to the Arduino.
3. Power on the Arduino and observe the traffic light cycle.

---

## Notes

- Adjust the timings in the code to simulate different traffic patterns.
- Use appropriate resistors to prevent damage to the LEDs.
- Ensure the Arduino board is powered properly.

---

## License

This project is open-source and available under the MIT License.
