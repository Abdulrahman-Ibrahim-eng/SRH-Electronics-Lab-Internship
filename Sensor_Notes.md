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

## Hardware setup:
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

## Sensor 2: KY-037 Microphone Sensor Module
### Basic information:
-Sensor name: KY-037 Microphone Sensor Module
-Purpose: Input sound signals 
-Interface: Analog
-Operating voltage: 5V
-Reference: https://sensorkit.joy-it.net/en/sensors/ky-037

### How it works:
-This sensor has two functional components on its circuit board: The front sensor unit, which physically measures the environment and outputs it as an analog signal to the second unit, the comparator. The comparator compares the measured value of the sensor with the value set on the rotary potentiometer and outputs a logical high signal on the digital pin and LED L1 if the value on the rotary potentiometer is exceeded.

## Hardware setup:
### Software setup:
- Platform: Arduino Uno
- Programming language: C
- Library: None required

### PIN connection:
<img width="661" height="675" alt="Screenshot 2026-01-29 222115" src="https://github.com/user-attachments/assets/7d9b27d8-8c72-4f03-adbb-40bb46001c58" />

### Arduino sketch:
// Declaration and initialization of the input pins
int analog_input = A0; // Analog output of the sensor
int digital_input = 3; // Digital output of the sensor
  
void setup () {
  pinMode(analog_input, INPUT);
  pinMode(digital_input, INPUT);
  Serial.begin(9600); // Serial output with 9600 bps
  Serial.println("KY-037 Noise detection");
}
  
// The program reads the current values of the input pins
// and prints them to the serial output
void loop () {
  float analog_value;
  int digital_value;
    
  // Current values are read out, converted to the voltage value...
  analog_value = analogRead(analog_input) * (5.0 / 1023.0); 
  digital_value = digitalRead(digital_input);
    
  //... and printed at this point
  Serial.print("Analog voltage value: "); 
  Serial.print(analog_value, 4);
  Serial.print(" V, \t Threshold value: ");
  
  if (digital_value == 1) {
      Serial.println("reached");
  }
  else {
      Serial.println("not yet reached");
  }
  Serial.println("----------------------------------------------------------------");
  delay(1000);
