# Sensor Notes
## Sensor 1: KY-034 LED Flash Module
### Basic information:
-Sensor name: KY-034 LED Flash Module
-Purpose: Lightning 
-Interface: Analog
-Operating voltage: 5V
-Reference: https://sensorkit.joy-it.net/en/sensors/ky-034

### How it works:
-Electric current flows through the diode causing and excitation of electrons in the diode and once they return to their initial energy level a photon is emitted

### Hardware setup:

### Software setup:
- Platform: Arduino Uno
- Programming language: C
- Library: None required

### PIN connection
<img width="634" height="707" alt="Screenshot 2026-01-23 205554" src="https://github.com/user-attachments/assets/8a31c207-2bf3-44ea-a05e-365bad8b87f1" />

### Arduino sketch:
int led = 13; // Declaration of the LED input pin
 
void setup() {
  pinMode(led, OUTPUT); // Initialization output pin for the LED
}
void loop() {
  digitalWrite(led, HIGH); // LED is switched on
  delay(4000); // Wait for 4 seconds
  digitalWrite(led, LOW); // LED is switched off
  delay(2000); // Wait for another two seconds
}
