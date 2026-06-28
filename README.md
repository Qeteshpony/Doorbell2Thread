# Doorbell2Thread

### Turning an old analog doorbell into a smart one... 

[![CI](https://github.com/Qeteshpony/Doorbell2Thread/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/Qeteshpony/Doorbell2Thread/actions/workflows/ci.yml)

![3D Render](https://qeteshpony.github.io/Doorbell2Thread/3D/Doorbell2Thread-3D_top.png)

[Hardware Documentation](https://qeteshpony.github.io/Doorbell2Thread)

# Hardware description

This is a very simple device that can be connected to an old analog intercom system to notify home assistant about someone ringing the bell. This was specifically made for the system in the house I live in but it might be compatible with yours as well - no guarantees though. 

I am using a small form factor ESP32-H2 module (Waveshare ESP32-H2 Mini) because the H2 is low power and the power supply for the intercom can't handle much current. 

There's also some protective circuitry since my first prototype got completely fried by induced voltages in the intercom cables. This version now runs stable and without problems. 

# Software

This is running on ESPHome. My configuration is available in this repo, see [doorbell.yaml](doorbell.yaml) (You of course have to add your secrets before using it...) 

This configuration is using the built in RGB led on the ESP-module to show the status. It's brightness can be tuned through Home Assistant to make it visible through the case if desired. 
