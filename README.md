I liked the idea of Tom's [Sensorbox v2](https://go.toms3d.org/sbr1) project, but when I built it I had performance and reliability issues that caused it to lose the Wi-Fi connection every few minutes.  Eventually I determined these issues were caused by the code handling the display, and started migrating the display code to LVGL.  It didn't take long for me to decide it'd be easier to start from scratch, I found Tom's code hard to follow.  That first attempt got the devices stable on my network, reliably reporting to Home Assistant.  That version was posted on [Printables](https://www.printables.com/model/1130249-3d-printer-emission-sensor-array-sensorbox-v2-lvgl) as a remix of Tom's model, to make it available to other people building his project.

This version adds support for [SEN5x](https://esphome.io/components/sensor/sen5x.html) sensors on the i2c_2 bus (the "extra" i2c positions on Tom's board).

My intention is to develop this into a project that can be used for both monitoring indoor air quality and local smart home control, while maintaining backwards compatibility with Tom's PCBs.  That effort will require a revised PCB to support touch screen control (ILI9341 display with XPT2046 touch screen controler) and human presence detection (HLK-LD2402), to facilitate automated control of lights and heat pumps depending on time of day, room mode, and room occupancy.

### Installation
Simply install these files, preserving directory structure, into /homeassistant/esphome/ on your HA server, then install to devices in the usual ESPHome way.  For multiple sensorboxes, simply make copies of sensorbox1.yaml, changing (at least) the ID for each instance.

Incorporates [MaterialDesign-Webfont](https://github.com/Templarian/MaterialDesign-Webfont).

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg