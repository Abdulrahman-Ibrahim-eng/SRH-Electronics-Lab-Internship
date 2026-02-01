# Sensor Notes
## Sensor 1: 
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

## Sensor 2: 
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

  ## Sensor 3: 
  ### Basic information:
  -Name: KY-40 Rotary Encoder
  -Purpose: Machine controls
  -Interface: Analog
  -Operating voltage: 5V
  -Reference: https://sensorkit.joy-it.net/en/sensors/ky-040

  ### How it works:
  -The state of the two outputs changes with each step, allowing the direction of rotation to be determined. The direction of rotation is determined by the sequence of the state changes of the outputs: Depending on which output changes state first, it is possible to detect whether the switch is turned clockwise or counterclockwise.

  ## Hardware setup:
  ### Software setup:
- Platform: Arduino Uno
- Programming language: C
- Library: None required

  ### PIN connection:
  <img width="875" height="722" alt="Screenshot 2026-01-31 145313" src="https://github.com/user-attachments/assets/2b5ea803-1e8a-4df8-be07-a9f94f646256" />

  ### Arduino sketch:

  ## Sensor 4:
  ### Basic information:
-Sensor name: KY-002 Vibration switch
-Purpose: Detect vibrations
-Interface: Analog
-Operating voltage: 3.3V,5.0V
-Reference: https://sensorkit.joy-it.net/en/sensors/ky-002

### How it works:
-The KY-002 shock and vibration sensor is a precise module for detecting shocks and vibrations. It consists of a conductive outer casing and an internal spring. In the event of shocks, the spring closes the contact to the outer casing and thus generates an electrical signal. This simple design enables reliable and fast detection of vibrations.

## Hardware setup:
### Software setup:
- Platform: Arduino Uno
- Programming language: C
- Library: None required

### PIN connection:
<img width="710" height="699" alt="Screenshot 2026-02-01 161733" src="https://github.com/user-attachments/assets/8878d171-79df-43b8-bf1b-57615046c83a" />

### Arduino sketch:
int vib = 10; // Declaration of the sensor input pin
int value; // Temporary variable
  
void setup ()
{
  pinMode(vib, INPUT); // Initialization sensor pin
  digitalWrite(vib, HIGH); // Activation of internal pull-up resistor
  Serial.begin(9600); // Initialization of the serial monitor
  Serial.print("KY-002 Vibration detection");
}
  
void loop ()
{
  // The current signal at the sensor is read out.
  value = digitalRead(vib); 
  // If a signal could be detected, this is displayed on the serial monitor.
  if (value == LOW) {
    Serial.println("Signal detected");
    delay(100); // 100 ms break
    }
}


  

  
