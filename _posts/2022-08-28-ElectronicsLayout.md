---
published: True
layout: post
title: "Electronics Layout Thoughts"
date: 2022-08-28 015:35.0 -0700
categories: Layout
author: James Alspach
---
Some basic notes on the electronics and how they need to be laid out.
{% capture string_with_newlines %}
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
    - include one to drain each tank?
## Micro Connections
- Temp sensors 1 wire bus
- Flow sensor - Analog?
    - 3 Analog in
- Level sensor - Analog?
    - 5 Analog in
    - Could I build a 1 wire or i2c version of this?
- Push buttons x5
    - Charlieplex? MCP23008?
- LED's x?
    - Charlieplex? MCP23008?
## Display / control
- LCD display in box for basic numbers
    - can we display a graph?
- Wireless connection back to the network
- Buttons like the current box
    - Hold to fill Sump
    - One each hold to drain tanks? (3 total)
    - Ability to turn off and on the pump




{% endcapture %}

{{ string_with_newlines | newline_to_br }}