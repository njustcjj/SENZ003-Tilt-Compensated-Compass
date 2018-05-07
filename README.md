# SENZ003-Tilt-Compensated-Compass

###### Translation

> For `English`, please click [`here.`](https://github.com/FizzyStudio/SENZ003-Tilt-Compensated-Compass/blob/master/README.md)

> For `Chinese`, please click [`here.`](https://github.com/FizzyStudio/SENZ003-Tilt-Compensated-Compass/blob/master/README_CN.md)

![](https://github.com/njustcjj/SENZ003-Tilt-Compensated-Compass/blob/master/pic/SENZ003.jpg "SENZ003")

### Introduction

> The LSM303DLH is a triple axis accelerometer combined with a triple axis magnetic sensor.
> This breakout board uses the LSM303DLH to give you the data you need to feed into a arduino microcontroller and calculate tilt-compensated output.

#### Application

- Compensated compassing
- Map rotation
- Position detection
- Motion-activated functions
- Free-fall detection
- Intelligent power-saving for handheld devices
- Display orientation
- Gaming and virtual reality input devices
- Impact recognition and logging
- Vibration monitoring and compensation


### Specification

* Power supply: 3.6~8V DC
- Chip: LSM303DLH
- ±1.3 to ±8,1 gauss magnetic field full-scale
- ±2 g/±4 g/±8 g dynamically selectable fullscale
- 16-bit data out
- I2C serial interface
- 2 independent programmable interrupt
- generators for free-fall and motion detection
- Embedded self-test
- Accelerometer sleep-to-wakeup function
- 6D orientation detection
- Dimensions: 20.5mmx20.5mm 
- Weight: 1g 

### Tutorial

#### Connection Diagram

![](https://github.com/FizzyStudio/SENZ003-Tilt-Compensated-Compass/blob/master/pic/SENZ003_connect.png "Connection Diagram") 

#### Sample Code

    #define SensorLED   13
    //Connect the sensor to digital Pin 3 which is Interrupts 1.
    #define SensorINPUT  3  

    unsigned char state = 0;

    void setup() {
      pinMode(SensorLED, OUTPUT);
      pinMode(SensorINPUT, INPUT);
      //Trigger the blink function when the falling edge is detected
      attachInterrupt(1, blink, FALLING);  
    }

    void loop() {
      if (state != 0) {
        state = 0;
        digitalWrite(SensorLED, HIGH);
        delay(500);
      } 
      else
        digitalWrite(SensorLED, LOW);
    }

    //Interrupts function  
    void blink() {
        state++;
    }


### Purchasing [*SENZ003-Tilt-Compensated-Compass*](https://www.ebay.com/).