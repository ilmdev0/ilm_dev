---
title: "Self Balancing Table"
date: false
draft: false
tags: [project]
publish: true
---

# Self Balancing Table


> [!failure] Problem
>During the summer, as we engage in outdoor activities such as parties, sunbathing, and hiking, we often face the challenge of finding a stable surface for our food, coffee cups, and water glasses. Outdoor terrains are typically uneven, making it difficult to place a regular table without compromising its level surface. This issue persists during winter activities in snowy conditions, where placing a conventional table becomes impractical due to the risk of the legs getting stuck.

> [!done] Solution and Benefits of the Self-Balancing Table:
>Our solution addresses these challenges by introducing a self-balancing table that can adapt to any uneven surface. The table automatically stabilizes itself, ensuring a level surface regardless of the field's irregularities. When transporting the table from one location to another, built-in sensors detect changes in the surface and adjust the height of the table legs accordingly, maintaining stability.


# Components Used:

- Arduino UNO
- XYZ Accelerometer Sensor
- 360-Degree Rotation Servo Motor
- Voltage Divider
- 3D Printed Parts
- Plywood Plate
- Stabilization Algorithm/Coding

### Slides

![[Image1.png]]
![[Image2.png]]
![[Image3.png]]
![[Image4.png]]

> ##### Final Output
![[Image5.jpg]]

> #### Code for servo motor
`Servo_Motor.ino`

```
#include <Servo.h>

Servo myservo1;
Servo myservo2;
Servo myservo3;

int pos = 0;

void setup() {
  myservo1.attach(9);
  myservo2.attach(10);
  myservo3.attach(11);
}

void loop() {
  // Move forward for 8 seconds
  for (int i = 0; i <= 180; i += 1) {
    myservo1.write(i);
    myservo2.write(i);
    myservo3.write(i);
    delay(44); // Adjust the delay for smoother motion
  }
  
  delay(8000); // Wait for 8 seconds

  // Move backward for 10 seconds
  for (int i = 180; i >= 0; i -= 1) {
    myservo1.write(i);
    myservo2.write(i);
    myservo3.write(i);
    delay(50); // Adjust the delay for smoother motion
  }

  delay(10000); // Wait for 10 seconds
}
```

> #### Code for accelerometer sensor
`Accelerometer_sensor.ino`

```
#include <math.h>
const int x_out = A1; /* connect x_out of module to A1 of UNO board */
const int y_out = A2; /* connect y_out of module to A2 of UNO board */
const int z_out = A3; /* connect z_out of module to A3 of UNO board */

void setup() {
  Serial.begin(9600); 
}

void loop() {
  int x_adc_value, y_adc_value, z_adc_value; 
  double x_g_value, y_g_value, z_g_value;
  double roll, pitch, yaw;
  x_adc_value = analogRead(x_out); /* Digital value of voltage on x_out pin */ 
  y_adc_value = analogRead(y_out); /* Digital value of voltage on y_out pin */ 
  z_adc_value = analogRead(z_out); /* Digital value of voltage on z_out pin */ 
  Serial.print("x = ");
  Serial.print(x_adc_value);
  Serial.print("\t\t");
  Serial.print("y = ");
  Serial.print(y_adc_value);
  Serial.print("\t\t");
  Serial.print("z = ");
  Serial.print(z_adc_value);
  Serial.print("\t\t");
  //delay(100);
  
  x_g_value = ( ( ( (double)(x_adc_value * 5)/1024) - 1.65 ) / 0.330 ); /* Acceleration in x-direction in g units */ 
  y_g_value = ( ( ( (double)(y_adc_value * 5)/1024) - 1.65 ) / 0.330 ); /* Acceleration in y-direction in g units */ 
  z_g_value = ( ( ( (double)(z_adc_value * 5)/1024) - 1.80 ) / 0.330 ); /* Acceleration in z-direction in g units */ 

  roll = ( ( (atan2(y_g_value,z_g_value) * 180) / 3.14 ) + 180 ); /* Formula for roll */
  pitch = ( ( (atan2(z_g_value,x_g_value) * 180) / 3.14 ) + 180 ); /* Formula for pitch */
  //yaw = ( ( (atan2(x_g_value,y_g_value) * 180) / 3.14 ) + 180 ); /* Formula for yaw */
  /* Not possible to measure yaw using accelerometer. Gyroscope must be used if yaw is also required */

  Serial.print("Roll = ");
  Serial.print(roll);
  Serial.print("\t");
  Serial.print("Pitch = ");
  Serial.print(pitch);
  Serial.print("\n\n");
  delay(1000);
}
```

> [!note] Note
> To run the code on Arduino IDE, you will need to install the library `Adafruit_Sensor` , `Servo-1.2.1` and `SparkFun_ADXL345_Arduino_Library`. You will final the full repository on my [github](https://github.com/SAJIB3489/Balancing_Table.git) and also simulation [video](https://amksavonia-my.sharepoint.com/:v:/g/personal/md_sajib_pramanic_edu_savonia_fi/EU7R_d-bmGZIj79L25YZF8MBw07vUwrip7E_vqRFEz2pSQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=6LyNJp)

