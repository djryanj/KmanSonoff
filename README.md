# BIG FAT NOTE: THIS REPO IS NOT YET WORKING ANY DIFFERENT FROM THE ORIGINAL. ALL I HAVE DONE AT THIS DATE IS FORK IT AND UPDATE README.MD.

KmanSonoff-Touch - Alternative firmware for Sonoff Switches with Added Support for Capacitive Touch

#### NOTE: This is a fork of the amazing [KmanOz/KmanSonoff](https://github.com/KmanOz/KmanSonoff) firmware for Sonoff devices. This fork adds support for a capacitive touch sensor on GPIO14.

#### Currently Supported Devices (More to come)

This fork was written with only one of the Sonoff devices in mind, the [Sonoff Basic](https://www.itead.cc/smart-home/sonoff-wifi-wireless-switch.html?acc=70efdf2ec9b086079795c442636b55fb; and it was originally developed/tested on a Wemos D1 mini.

## Configuration

**1. Clone the Repository**

Clone the **KmanSonoff-Touch** repository to your local machine. Copy the required version for your switch to your Arduino directory.

``` bash
$ git clone https://github.com/djryanj/KmanSonoff-Touch
```
**2. Clone the LMROY version of the mqtt library**

I use the [lmroy](https://github.com/Imroy/pubsubclient) version of this excellent mqtt library, mainly because it supports QOS1 and keepalive settings right from within the sketch. No other modifications to library files are necessary.

It's currently setup to use only v3.1.1 of the mqtt standard and will only work on that version broker unless you modify the code so make sure your broker is setup to use v3.1.1 of the mqtt standard and not v3.1.

**FOR ALL THE PEOPLE THAT SKIP THIS STEP, DON'T. YOU CANNOT USE OTHER MQTT LIBRARIES**

``` bash
$ git clone https://github.com/Imroy/pubsubclient
```

**3. Modify the details in the Arduino code (config.h) to your specific details and environment. (THIS IS IMPORTANT)**

To start off, change the "WIFI_SSID, WIFI_PASS, MQTT_SERVER, MQTT_PORT, MQTT_USER, MQTT_PASS in the Arduino code provided to suit your environment. 

``` bash
#define MQTT_SERVER     "192.168.0.100"                      // mqtt server
#define MQTT_PORT       1883                                 // mqtt port
#define MQTT_TOPIC      "home/sonoff/living_room/1"          // mqtt topic (Must be unique for each Sonoff)
#define MQTT_USER       "user"                               // mqtt user
#define MQTT_PASS       "pass"                               // mqtt password
#define WIFI_SSID       "homewifi"                           // wifi ssid
#define WIFI_PASS       "homepass"                           // wifi password
```

Additionally other parameters can be changed in the file at your discretion like whether or not you wish to remember the last relay state, retain mqtt messages, update frequecy for WiFi retries etc. See "config_sc.h or config_mc.h" for all options.

## Flashing the Firmware

tbd

## HomeAssistant Integration

Same as with the original firmware. The addition of the capacitive sensor does not alter HomeAssitant integrations at all.

## Commands and Operation

**1. Commands**
tbd

**2. Operation**

As per the original firmware (add here)

## OTA Updates
tbd

## Versions

tbd

## MIT License

Copyright (c) 2017

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Conclusion

Thanks!
