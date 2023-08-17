# Room Occupancy Monitoring System

This Arduino project implements a simple room occupancy monitoring system. It uses two input buttons to track the entry and exit of people from a room, and an array of LEDs to indicate the number of people currently in the room. The system provides real-time updates on the occupancy status of the room through the serial monitor.

## Features

- Tracks the entry and exit of people from a room using input buttons.
- Displays the current occupancy status on an array of LEDs.
- Provides real-time updates through the Arduino serial monitor.

## Hardware Requirements

- Arduino board (e.g., Arduino Uno)
- 5 LEDs
- 2 push buttons
- 7 resistors (for LEDs and buttons)
- Jumper wires

## Setup

1. Connect the LEDs to digital pins 3 through 7 on the Arduino board.
2. Connect the push buttons to digital pins 8 and 9 on the Arduino board.
3. Connect resistors in series with the LEDs and push buttons for current limiting (appropriate resistance values should be chosen based on LED and button specifications).
4. Upload the provided code (`room_occupancy_monitor.ino`) to the Arduino board using the Arduino IDE.
5. Open the Arduino serial monitor at a baud rate of 9600 to observe the occupancy updates.

## Usage

1. When a person enters the room, press the entry button (connected to pin 8). The system will increment the occupancy count and illuminate the corresponding LED.
2. When a person exits the room, press the exit button (connected to pin 9). The system will decrement the occupancy count and turn off the corresponding LED.
3. Real-time occupancy updates will be displayed on the serial monitor.

## Code Explanation

The Arduino sketch contains two main functions: `setup()` and `loop()`. The `setup()` function initializes the pins for LEDs and buttons, as well as starts the serial communication. The `loop()` function continuously monitors the status of the buttons and updates the occupancy count and LED array accordingly.

The `show()` function is responsible for displaying the current occupancy status on the serial monitor.

## Future Enhancements

This project can be expanded by adding more advanced features such as:
- Using a display (LCD or OLED) to show the occupancy count.
- Implementing a time-based occupancy tracking system.
- Adding a sensor to detect motion or presence for more accurate occupancy detection.
- Storing and analyzing historical occupancy data.

Feel free to modify and enhance the code to suit your specific requirements and hardware components.

## License

This project is licensed under the [MIT License](LICENSE).

