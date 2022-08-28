# ESPHome Modbus configuration for Schneider iEM3155 Energy Meter

This is my production configuration as a complete ESPHome example for the iEM3155 Energy Meter.

Extremely easy, full Home Assistant integration using ESPHome as wireless Modbus node. 

- Ensure that Com.Protection in the device is DISABLED.
    * Com.Protection is ENABLED by default !!
    * Otherwise partial reset of daily energy import registers will be ignored by the device (id: daily_energy_import_total + 3 x daily_energy_import_lX)
- My iEM3155 device configuration:
    * Serial: 19200, EVEN, 1 (default)
    * Slave address: 0x01


The devide also offers some additional interesting features that might be useful for others. Tariff/tariff rates and overload alarm. There's also both a digital input and output port that can be utilized as well.

Check the iEM3155 user manual/technical datasheet for further info:

https://download.schneider-electric.com/files?p_Doc_Ref=DOCA0005EN&p_enDocType=User+guide&p_File_Name=DOCA0005EN-13.pdf
