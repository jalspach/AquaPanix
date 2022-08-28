---
published: True
layout: post
title: "Electronics Layout Thoughts"
date: 2022-08-28 015:35.0 -0700
categories: Layout
author: James Alspach
---
Some basic notes on the electronics and how they need to be laid out.  

# Overall Plan  

Everything needs to connect back to a micro so that:
1. It can be monitored by MQTT
2. It can be monitored by local network
3. It can be controlled by local network

## What are we sensing  

- Flow sensor into top tube
- Temperature sensor at output of first tube
- Level sensor at output of first tube
- Flow sensor into second tube
- Temperature sensor at output of second tube
- Level sensor at output of second tube
- Flow sensor out of first tube and into fish tank
- Temperature sensor in fish tank
- Level sensor
- Temperature sensor in filter
- Level sensor in filter?
- Temperature sensor in sump
- Level sensor in sump
- Electronic solenoid valve from city water to sump
    - include one to drain each tank as well?  
- Total power draw through the sensing transformer
    - Analog? in  
- Light sensors (x3)
    - To detect open tanks 
- Buzzer


## Microcontroller Connections  

- Temp sensors
    - 1 wire bus
- Flow sensor
    - 3 Analog? in
- Level sensor
    - 5 Analog? in
    - Could I build a 1 wire or i2c version of this?
- Push buttons x5
    - Charlieplex? MCP23008?
- LED's x?
    - Charlieplex? MCP23008?
_ Relays for Pump and solenoid connections
    - 4 low volt for solenoids
    - 1 high volt for pump
- Current sensor
    - Analog in
- Light sensors
    - Analog in (x3)
    - could I simplify this to a digital output and then run it through the MCP23008?
- Buzzer
    - Analog output


## Display / control  

- LCD display in box for basic numbers
    - can we display a graph?
- LED's
    - Outside / inside box for general status
- Wireless connection back to the network
- Buttons like the current box
    - Hold to fill sump manually (this should generally be automatic) (1 total)
    - Hold to drain tanks? (3 total one per tank)
    - Ability to turn off / on the pump  

## Power  

- 5VDC / 9VDC for microcontrollers
- 12 V for 24 V solenoids?
- 120 VAC for pump
- Breaker w/ GFCI  

## To Build
Need to build one or two boards:
- I/O Board
    - Push terminals
        - 1Wire (include switchable resistor)
        - GPIO connectivity for external relays (keeps high voltage off of the board)
        - Analog inputs
        - Power from power-supply
    - RS232 Serial Port
    - USB port (extended from Micro)
    - CAN Bus (?)
    - Buttons
    - LCD
    - Buzzer
    - LED's
    - External LED drivers
    - Push terminals for external LED's
    - Header that is mapped pin-to-pin to the Micro for easy connection

