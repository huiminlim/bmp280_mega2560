# Interfacing BMP280 sensor in C - Arduino Mega

This repo contains test code to verify porting of Arduino's SPI and Adafruit's BMP280 C++ library to C.

Development was done in Atmel Studio 7.0 and tested on an Arduino Uno with ATmega2560 microcontroller.

This is part of FYP project to use Bosch's BMP280 sensor in C.

## Credits

Libraries are adapted from:

* [Arduino SPI library](https://github.com/arduino/ArduinoCore-avr/tree/master/libraries/SPI)

* [Adafruit's BMP280 library](https://github.com/adafruit/Adafruit_BMP280_Library)

Credits goes to them.

## BMP280

Bosch's BMP280 humidity sensor is used and the datasheet can be found [here](https://www.bosch-sensortec.com/products/environmental-sensors/pressure-sensors/pressure-sensors-bmp280-1.html).

## Dependencies

Development was done in Atmel Studio 7.0 and certain Atmel Software Framework (ASF) libraries were used.

They include:

* [Delay Routine](https://asf.microchip.com/docs/latest/saml21/html/group__group__common__services__delay.html)

* [IOPORT Service](https://asf.microchip.com/docs/latest/saml21/html/group__ioport__group.html#gabc09edad7c3187dec63ce47e6f1b3c51)

## Wiring

The sensors are wired to the Arduino Mega board as such:

![Wiring](wiring.PNG)

## Expected Output

Currently, only the temperature reading can be obtained as the FYP only requires the temperature reading.

To ensure that the temperature sensor reads the correct temperature value, ensure that the correct sampling settings are configured.

As of now, the code does not support setting the sampling setting, so run the Arduino IDE sketch to configure the sampling settings before flashing this code in the microcontroller to read from the sensor.

The output should look like this:

![Expected output](Capture_mega.PNG)
