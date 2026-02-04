# Sensor Notes
## Sensor 1: 
### Basic information:
- Sensor name: KY-034 LED Flash Module
- Purpose: Lightning 
- Interface: Digital
- Operating voltage: 5V
- Reference: https://sensorkit.joy-it.net/en/sensors/ky-034

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
<img width="928" height="448" alt="Screenshot 2026-02-04 191405" src="https://github.com/user-attachments/assets/a69fed66-bd70-4724-a5e4-f5925d944c6a" />

## Sensor 2: 
### Basic information:
- Sensor name: KY-037 Microphone Sensor Module
- Purpose: Input sound signals 
- Interface: Analog and digital(hybrid interface)
- Operating voltage: 5V
- Reference: https://sensorkit.joy-it.net/en/sensors/ky-037

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
<img width="628" height="622" alt="Screenshot 2026-02-04 191542" src="https://github.com/user-attachments/assets/d327e6b5-4fa2-4997-9200-e8344d59878d" />

  ## Sensor 3: 
  ### Basic information:
  -Name: KY-40 Rotary Encoder
  -Purpose: Machine controls
  -Interface: Digital
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
  <img width="970" height="620" alt="Screenshot 2026-02-04 191636" src="https://github.com/user-attachments/assets/354b9ee5-6681-4b55-bb6f-015722b97289" />

  ## Sensor 4:
  ### Basic information:
-Sensor name: KY-002 Vibration switch
-Purpose: Detect vibrations
-Interface: Digital
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
<img width="563" height="399" alt="Screenshot 2026-02-04 191729" src="https://github.com/user-attachments/assets/13bb6518-4a61-4e30-92b3-b7d26291c97c" />

## Sensor 5:
### Basic information:
-Sensor name: KY-052 
-Purpose: Temperature and barometric pressure sensor
-Interface: Digital
-Operating voltage: 3.3V, 5.0V
-Reference: https://sensorkit.joy-it.net/en/sensors/ky-052

### How it works:
-The BMP280 is a versatile sensor that measures both barometric pressure and temperature and outputs the results via the I2C bus. With this sensor you can capture precise air pressure and temperature values, making it ideal for applications such as weather stations, altimeters and mobile devices.

## Hardware setup:
### Software setup:
- Platform: Arduino Uno
- Programming language: C
- Library: Adafruit BMP280

### PIN connection:
<img width="952" height="681" alt="Screenshot 2026-02-04 194149" src="https://github.com/user-attachments/assets/fdb3afc9-5b0b-4230-a7a6-d45eabc592a5" />

### Arduino sketch:
<img width="389" height="730" alt="Screenshot 2026-02-04 201017" src="https://github.com/user-attachments/assets/e2440098-6d7a-4e5b-95a5-cdcad10556e6" />

## Sensor 6:
### Basic information:
-Sensor name: KY-023 
-Purpose: Joystick Module(X-Y axis)
-Interface: Analogue
-Operating voltage: 5V
-Reference: https://sensorkit.joy-it.net/en/sensors/ky-023

### How it works:
-This module detects the X and Y position of a joystick and outputs this as an analog voltage at the output pins. A separate potentiometer is installed for each axis, X and Y. In the idle state, the potentiometer is in the middle, which means that the resistances and therefore the voltages are the same.
-If the position of the X or Y axis is changed, the resistances change depending on the new position. This change in resistance leads to different voltage values that can be measured between the resistors. This allows the exact position of the axis to be determined.

## Hardware setup:
### Software setup:
- Platform: Arduino Uno
- Programming language: C
- Library: None required

###  PIN connection:
<img width="957" height="718" alt="Screenshot 2026-02-04 201503" src="https://github.com/user-attachments/assets/8bbddb68-7fde-4e1f-8e8a-70dea6fa6269" />

### Arduino sketch:
<img width="506" height="690" alt="Screenshot 2026-02-04 201614" src="https://github.com/user-attachments/assets/c82e9982-95c1-4a43-af9b-aabdad2ffb37" />

## Sensor 7:
### Basic information:
-Sensor name: KY-006
-Purpose: Passive Piezo-Buzzer
-Interface: Analogue
-Operating voltage: 3.3V, 5.0V
-Reference: https://sensorkit.joy-it.net/en/sensors/ky-006

### How it works:
With this module, you can generate different sounds by controlling the passive piezo buzzer with PWM signals. PWM signals are special electrical signals that can be sent at different frequencies to generate different sounds. The buzzer can generate sounds in the range of 1.5 kHz to 2.5 kHz. 

## Hardware setup:
### Software setup:
- Platform: Arduino Uno
- Programming language: C
- Library: None required

###  PIN connection:
<img width="766" height="749" alt="Screenshot 2026-02-04 204940" src="https://github.com/user-attachments/assets/eb03921b-0149-46fe-ac01-35d623872bcc" />

## Arduino sketch:
<img width="876" height="692" alt="Screenshot 2026-02-04 210330" src="https://github.com/user-attachments/assets/e3048cb8-661e-482d-8281-67c8f2a3d393" />









  

  
