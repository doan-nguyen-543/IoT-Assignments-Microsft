## Sensor: MPU6050 - Accelerometer + Gyroscope
1. **What is does?**
- It provides 6DOF: 3-axis accelerometer and a 3-axis gyroscope. This allows an IoT device to track complex movement in 3D space with high precision.
2. **The electronics/ hardware used in**
The MPU6050 contains two distinct MEMS (Micro-Electro-Mechanical Systems) structures on a single silicon die:
- Accelerometer: Uses the same capacitive sensing principle as the ADXL345 (suspended mass).
- Gyroscope: Uses the Coriolis Effect. Inside the chip, tiny silicon parts are kept in constant vibration. When you rotate the sensor, the Coriolis force causes these vibrating parts to shift laterally. This shift is detected as a change in capacitance and converted into an angular velocity reading.
- DMP (Digital Motion Processor): This is the "secret sauce." It’s an onboard processor that handles the heavy math of combining (fusing) the accel and gyro data so your main microcontroller doesn't have to.
3. **Is it analog or digital?**
- It is Digital. It features 16-bit Analog-to-Digital Converters (ADCs) for every channel. It communicates with your dev kit exclusively via the I2C protocol.
4. **What the units and range of inputs or measurements is?**
Because it has two sensors in one, it has two sets of units:
* Accelerometer (Linear Motion)
- Units: $g$ (gravitational force).
- Range: User-programmable to $\pm 2g, \pm 4g, \pm 8g,$ or $\pm 16g$.
* Gyroscope (Rotational Motion)
- Units: °/s (degrees per second).
- Range: User-programmable to $\pm 250, \pm 500, \pm 1000,$ or $\pm 2000$ °/s.

## Actuator: LED
1. **What is does?**
- An LED converts electrical energy directly into light energy. In an IoT system, it acts as a user interface output—providing status updates, warnings, or illumination based on sensor data.
2. **The electronics/ hardware used in**
- An LED is a semiconductor device. It consists of a "P-N junction" made from materials like Gallium Arsenide. When current flows through the junction, electrons fall into vacancies in the lower energy levels. As they fall, they release energy in the form of photons.
3. **Is it analog or digital?**
* It is technically Analog in nature (it reacts to varying levels of current), but in IoT dev kits, it is used in two ways:
- Digital: Turned fully HIGH (on) or LOW (off).
- Quasi-Analog (PWM): By using Pulse Width Modulation, you can pulse the LED on and off so fast that it appears to dim or brighten, simulating an analog behavior.
4. **What the units and range of inputs or measurements is?**
- Input Units: Measured in Volts (V) and Milliamps (mA). Most standard LEDs require 1.8V to 3.3V and roughly 20mA of current.
- Output Units: Measured in Lumens (lm) for brightness or Mcd (millicandela) for luminous intensity.
- Wavelength: Measured in Nanometers (nm), which determines the color (e.g., ~650nm for Red, ~450nm for Blue).