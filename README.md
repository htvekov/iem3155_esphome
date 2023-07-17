# ESPHome Modbus configuration for Schneider iEM3155 Energy Meter v1.1

![iem3155](https://github.com/htvekov/iem3155_esphome/blob/main/iem3155.png)

### Revision:
- **v1.1** (2023-07-17)
   * Improved documentation
   * Code revised to be more resilient to reboots (not power cycles)
   * Solar export total base value is now retained in RTC memory
   * Added two more sensors:
      * Daily solar power self-consumption
      * Daily solar power export total 

This repo contains my production configuration and serves as a complete ESPHome example for the iEM3155 Energy Meter.

Extremely easy, full Home Assistant integration using ESPHome as wireless Modbus node. 

> ***Note***
> 
> Ensure that Com.Protection in the device is *DISABLED* - Com.Protection is *ENABLED* by default !!
>
> Otherwise partial reset of daily energy import registers will be *IGNORED* by the device (id: daily_energy_import_total + 3 x daily_energy_import_lX)

- iEM3155 device configuration:
    * Serial: 19200, EVEN, 1 (default)
    * Slave address: 0x01
- ESP8266 module:
    * [Wemos D1 Mini v3](https://www.aliexpress.com/item/32845253497.html)
- RS485 modbus module
    * [XY-017](https://www.aliexpress.com/item/1005002863807590.html) 'Noname' AliExpress RS485 module

The devide also offers some additional interesting features that might be useful for others. Tariff/tariff rates and overload alarm. There's also both a digital input and output port that can be utilized as well.

Check the iEM3155 user manual/technical [datasheet](https://download.schneider-electric.com/files?p_Doc_Ref=DOCA0005EN&p_enDocType=User+guide&p_File_Name=DOCA0005EN-13.pdf) for further info

![Wemos D1 Mini v3](https://github.com/htvekov/iem3155_esphome/blob/main/Wemos_D1_Mini_v3.PNG) ![XY-017 TTL/RS485 module](https://github.com/htvekov/iem3155_esphome/blob/main/XY-017.jpg)
