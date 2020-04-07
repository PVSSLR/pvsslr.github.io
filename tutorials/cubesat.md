<img src="images/prototype1.jpg" width="180" height ="180">  <img src="images/cub.png" width="180" height ="180"> 

Note:- The above pictures are the prototype 1 & 2 of the CubeSat.

# CUBESAT USING ARDUINO 

A Picosatellite is made using the Arduino development board with an open-source architecture. The project aims to replicate the working mechanism of a CubeSat. 

## Getting Started

The core components of the picosatellite are chassis, Micro Controller Unit, Sensors. We will design and fabricate the CubeSat chassis using 3D printer technology. To receive and detect various data from IMU sensors. Work has been done for this project to get data from the sensors using Arduino IDE and python is used to visualize, plot live data graph, and to store data.

### Prerequisites

The prerequisites are given below
```
*Python IDE - pycharm, wing pro 6/7
*Arduino IDE 
*Fritzing (Not Mandatory)
```
### Installing

* Install any Python IDE - [PyCharm](https://www.jetbrains.com/pycharm/) 
* Install Arduino IDE - [Arduino IDE](https://www.arduino.cc/en/main/software)

### Arduino libraries 

* [DHT sensor library]( https://github.com/adafruit/DHT-sensor-library)
* SD library
* SPI library
* RadioHead
* MPU6050

### Python libraries 

 * pygame
 * pyserial
 * opengl
 * matplotlib
 
 ## Deployment 
 ### A. To Visualize the movements  and to read sensor data 
  1. Connect the circuit for MPU-6050 and dht11 separately.
  2. Connect the Arduino with Laptop/PC.
  3. Download or install all the required libraries for Python and Arduino.
  4. Make sure you choose the correct port and board in Arduino IDE.
  5. Upload the ``IMU_Cubesat.ino`` to the Arduino IDE.
  (NOTE:- You don't need to upload the sketches to Arduino board every single time)
  6. Run the ``main.py`` in any Python IDE.
  7. Go to line 10 and modify ``YOUR_PORT_NO`` to the one you selected in Arduino IDE.
  
```
  ser = serial.Serial('YOUR_PORT_NO', 38400, timeout=1)
  ser = serial.Serial('COM7', 38400, timeout=1)
 ```
 ### B. To store sensor data on SD card
   1. Upload the ``Cubesat_SD.ino`` to the Arduino IDE.
   2. The code can be modified based on the sensor which you use.
   
 ### C. To plot live graph 
   1. Upload the ``Cubesat_Live_Graph.ino`` to the Arduino IDE.
   2. Run the ``Cubesat_Live_Graph.py`` in any python IDE.

(NOTE:-I have used dht11 sensor as an example to store data and plot live graph. You can include the sensors of your wish and modify the code)

## Acknowledgments

I want to thank Jet Aerospace Aviation Research Center for their support and contribution.

### NOTE
The codes have been taken from various online sources and has been modified. The project is only for educational purpose. I believe this could help undergraduates and beginners who are into Cubesat & Arduino.


 
 
