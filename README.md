# Arduino BME280 NodeMCU

Working example. Main code from <https://platformio.org/lib/show/166/Adafruit%20BME280%20Library> and with tips to get it working on a NodeMCU <https://github.com/optio50/ESP8266-NodeMCU-12E-with-BME280>

## Setup

|BME-280|NodeMCU|comments|
|---|---|---|
|VIN|3V|
|GNFD|G|
|SCL|D4|
|SDA|D3|

Code changes.

Add to `setup()`

```text
    Wire.begin(D3, D4); // Make sure you have D3 & D4 hooked up to the BME280
    Wire.setClock(100000);
    status = bme.begin(0x76);
```

