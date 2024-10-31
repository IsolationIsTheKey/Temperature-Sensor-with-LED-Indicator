![Preview](CADpreview.jpeg)


Temperature Sensor with LED Indicator  
University: Technical University of Cluj-Napoca  
Course: CAD Techniques  
Author: Daniil Zabunov  
Year: 2023  

Project Overview

This project involves designing a temperature sensor circuit with LED signaling, intended to indicate the temperature level within a predefined range.  
The LED lights up when the temperature falls between 0°C and 80°C, providing a visual feedback to the user. The circuit was developed using OrCAD and consists of five main design blocks.  

Project Components

1. Power Supply and Current Mirror

The circuit utilizes a single power source (Vcc = 15V) and includes a current mirror to provide a constant current to the sensor.   
The current through the sensor was set to 10 mA, which determined the value of resistor R1 to be 143 kOhms.  

2. Temperature Sensor

The temperature sensor provides an output voltage corresponding to the temperature within the circuit.  
It operates within a resistance range of 12k to 22k Ohms, with an output voltage from 1.2V to 2.2V based on the current (IRef = 10 mA).  

3. Differential Amplifier

The differential amplifier lowers the sensor output voltage close to 0V to fit within the specified range of [0V; Vcc - 2V].  
With a reference voltage (V2) set to 1.2V and a gain factor of 13, the amplifier output varies from 0V to approximately 12.68V.  

4. Comparators

The output from the amplifier is fed into three comparators, which control the LED based on threshold voltages. The comparators are configured with two threshold voltages:  
Low threshold (1.15V) for 10°C.  
High threshold (10.35V) for 90°C.  
The LED lights up when the sensor voltage is within these limits, providing the user with an indicator of the temperature range. The comparators use resistive dividers to set the thresholds.  

5. LED Signaling

The LED, driven by a current of 20 mA, is designed to light up when the output voltage is within the threshold range.  
Resistor R17, calculated as 370 Ohms, limits the current through the LED.  

Simulation Results

The circuit was simulated, and the LED correctly turns on and off according to the set temperature thresholds.  
The output signal from the final comparator exhibits a trapezoidal shape due to the Slew Rate of the operational amplifiers used (LM124).  

Additional Information

The project documentation includes detailed calculations, schematics, and simulation results for each design block, providing insights into the operational characteristics of the circuit.  
The bibliography lists relevant resources and references used in the design process.  
