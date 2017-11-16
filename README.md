# AWS IoT App Hackathon
Repo to house the information relating to my teams implementation for the [AWS IoT App Hackathon](https://awsiot.devpost.com)

## Setup Guide

### ESP32 / ESP8266

### Schematic

![images/esp32-design.png](images/esp32-design.png)

### Flashing

Our design utilizes a ESP32 or ESP8266 microcontroller. The code we used to flash our board can be found in the [t04glovern/esp32-mqtt-publish](https://github.com/t04glovern/esp32-mqtt-publish) repository.

More indepth instructures can be found in that projects README, however the outcome from flashing that code to your board will be a stream of data similar to the following (depending on your personal configuration).

```bash
ntp [Connected]
aws [Connected]
aws-sub [Connected]
accl [Connected]
aws-pub [Success]: {"thing_id":"thing-01","timestamp":1510856411,"accl_x":-0.857124,"accl_y":3.351882,"accl_z":15.05474,"accl_mag":15.44717,"accl_fft":[1.479036,0.612483,0.850653,0.894927,0.906535,0.942905]}
aws-pub [Success]: {"thing_id":"thing-01","timestamp":1510856412,"accl_x":0.684742,"accl_y":2.169147,"accl_z":16.08904,"accl_mag":16.24903,"accl_fft":[0.699518,0.672761,0.895605,0.908498,0.956246,0.956738]}
aws-pub [Success]: {"thing_id":"thing-01","timestamp":1510856413,"accl_x":-1.120486,"accl_y":0.445322,"accl_z":13.00051,"accl_mag":13.05631,"accl_fft":[2.676121,0.61359,0.800661,0.848166,0.870695,0.904833]}
aws-pub [Success]: {"thing_id":"thing-01","timestamp":1510856415,"accl_x":-0.263362,"accl_y":-0.138864,"accl_z":13.2543,"accl_mag":13.25764,"accl_fft":[0.40734,0.631146,0.803048,0.868581,0.884759,0.895562]}
```

The JSON playload being printed to serial is the payload sent to AWS IoT over its MQTT provider.

###
