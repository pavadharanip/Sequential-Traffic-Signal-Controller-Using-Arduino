📌 Project Overview

This project simulates a basic traffic signal system using an Arduino UNO and three LEDs: red, yellow, and green. The Arduino controls each LED according to a programmed sequence and time delay, demonstrating how traffic lights operate.

🎯 Objectives

- Understand Arduino UNO programming.
- Learn digital output control using GPIO pins.
- Understand LED connections and current-limiting resistors.
- Implement sequential control using programmed delays.
- Gain practical knowledge of embedded systems.

🛠️ Components Required

Component| Quantity
Arduino UNO| 1
Red LED| 1
Yellow LED| 1
Green LED| 1
220 Ω or 330 Ω resistors| 3
Breadboard| 1
Male-to-male jumper wires| 5 or more
USB cable| 1

🔌 Circuit Connections

LED| Arduino Pin
Red LED| Digital pin 10
Yellow LED| Digital pin 9
Green LED| Digital pin 8

Connection instructions:

- Connect each Arduino digital pin to the corresponding LED through its own 220 Ω or 330 Ω resistor.
- Connect the short leg (cathode) of each LED to the common GND rail.
- Connect the breadboard's GND rail to Arduino GND.

💻 Arduino Source Code

int red = 10;
int yellow = 9;
int green = 8;

void setup() {
  pinMode(red, OUTPUT);
  pinMode(yellow, OUTPUT);
  pinMode(green, OUTPUT);
}

void loop() {
  // Red light - STOP
  digitalWrite(red, HIGH);
  digitalWrite(yellow, LOW);
  digitalWrite(green, LOW);
  delay(5000);

  // Green light - GO
  digitalWrite(red, LOW);
  digitalWrite(yellow, LOW);
  digitalWrite(green, HIGH);
  delay(5000);

  // Yellow light - GET READY
  digitalWrite(red, LOW);
  digitalWrite(yellow, HIGH);
  digitalWrite(green, LOW);
  delay(2000);
}

⚙️ Working Principle

1. The Arduino initializes pins 10, 9, and 8 as outputs.
2. The red LED turns ON for 5 seconds to indicate STOP.
3. The green LED turns ON for 5 seconds to indicate GO.
4. The yellow LED turns ON for 2 seconds to indicate GET READY.
5. The sequence repeats continuously.

⏱️ Traffic Signal Timing

Signal| Duration| Meaning
🔴 Red| 5 seconds| Stop
🟢 Green| 5 seconds| Go
🟡 Yellow| 2 seconds| Get ready

▶️ How to Run the Project

1. Connect the LEDs, resistors, and Arduino UNO according to the connection table.
2. Connect the Arduino UNO to a computer using a USB cable.
3. Open Arduino IDE and paste the source code.
4. Select Tools → Board → Arduino UNO.
5. Select the correct port under Tools → Port.
6. Click Upload and observe the LED sequence.

📸 Project Images

Add your circuit photo to the repository and update the filename below to match your uploaded image.

"Arduino Traffic Light Circuit" (images/traffic-light-circuit.jpg)

📚 Concepts Learned

- Embedded systems
- Microcontroller programming
- Digital input/output (GPIO)
- LED interfacing
- Timing control using "delay()"
- Basic circuit design

🚀 Future Enhancements

- Add a pedestrian crossing button.
- Include a buzzer for pedestrian alerts.
- Display a countdown timer.
- Build a miniature traffic signal model.

🏁 Conclusion

This project demonstrates a simple traffic signal simulation using Arduino UNO and LEDs. It helps beginners understand digital output control, sequential programming, and basic embedded system development.

Note: This is an educational prototype, not a controller for real road traffic signals.

🔖 Technologies Used

- Hardware: Arduino UNO, LEDs, resistors, breadboard
- Software: Arduino IDE
- Programming language: Arduino C/C++
