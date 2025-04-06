OpenBook eReader

This project is a minimalist eBook Reader called OpenBook, built around the ESP32-C6 platform. The device is contains:

  A 7.5-inch e-paper display

  A Li-Po battery

  USB-C charging

  Navigation buttons

The design focuses on energy efficiency and ease of use, featuring a simple interface managed via GPIOs. The primary goal is to provide an optimal e-reading experience with low power consumption and a comfortable display.

Block diagram can be found in images.


| **Component** | **Details** |
|---------------|-------------|
| **MCU** | ESP32-C6 – supports Wi-Fi 6, BLE, Zigbee, and Thread |
| **Display** | 7.5-inch E-Paper (800 x 480 resolution, ~44g) |
| **Sensors** | BME688 – measures gas, humidity, temperature, and pressure |
| **Storage** | External NOR Flash 64MB (SPI) <br> SD Card (SPI) for extra storage |
| **Power Supply** | Battery: CELLEVIA BATTERIES LP584174 (3.7V, 1800mAh) <br> LDO Voltage Regulator for a steady 3.3V |
| **RTC** | Real-Time Clock for keeping time even when powered off |
| **Charging** | MCP73831T – charges via USB-C |
| **Extras** | Test Pads for debugging <br> Qwiic interface for easy module expansion |






Bill of Materials:

| **Component**                          | **Supplier**             | **Link**                                                                                           |
|----------------------------------------|--------------------------|----------------------------------------------------------------------------------------------------|
| 112A-TAAR-R03_ATTEND                    | Comet                    | [Buy](https://www.comet.com/parts/112A-TAAR-R03_ATTEND)                                             |
| 744043680IND                            | Mouser                   | [Buy](https://www.mouser.com)                                                                        |
| ADAFRUIT_LEDCHIP                        | SnapMagic                | [Buy](https://www.snapmagic.com/parts/ADAFRUIT_LEDCHIP)                                             |
| BD5229G-TR                              | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/BD5229G-TR)                                     |
| BUTTON_CUSYOMV1                         | Panasonic                | [Buy](https://www.panasonic.com)                                                                     |
| CPH3225A                               | SnapMagic                | [Buy](https://www.snapmagic.com/parts/CPH3225A)                                                      |
| DS3231SN                                | SnapMagic                | [Buy](https://www.snapmagic.com/parts/DS3231SN)                                                      |
| EAGLE-LTSPICE_CC0402                     | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/EAGLE-LTSPICE_CC0402)                           |
| ESP32-C6-WROOM-1-N8                      | SnapMagic                | [Buy](https://www.snapmagic.com/parts/ESP32-C6-WROOM-1-N8)                                           |
| ESP32_WROVER_AVX                         | Mouser                   | [Buy](https://www.mouser.com)                                                                        |
| ESP32_WROVER_BME680_BME680               | SnapMagic                | [Buy](https://www.snapmagic.com/parts/ESP32_WROVER_BME680_BME680)                                    |
| ESP32_WROVER_EAGLE-LTSPICE_C             | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/ESP32_WROVER_EAGLE-LTSPICE_C)                   |
| ESP32_WROVER_EAGLE-LTSPICE_R             | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/ESP32_WROVER_EAGLE-LTSPICE_R)                   |
| ESP32_WROVER_SPARKFUN-DISCRETESEMI        | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/ESP32_WROVER_SPARKFUN-DISCRETESEMI)              |
| ESP32_WROVER_SPARKFUN-IC-POWER_SOT23-5     | Mouser                   | [Buy](https://www.mouser.com)                                                                        |
| ESP32C6_VARISTORCN1812                   | Mouser                   | [Buy](https://www.mouser.com)                                                                        |
| FH34SRJ24S05SH99                         | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/FH34SRJ24S05SH99)                             |
| MAX17048G+T10                            | SnapMagic                | [Buy](https://www.snapmagic.com/parts/MAX17048G+T10)                                                 |
| MBR0530                                  | Mouser                   | [Buy](https://www.mouser.com)                                                                        |
| PGB1010603MR                             | SnapMagic                | [Buy](https://www.snapmagic.com/parts/PGB1010603MR)                                                  |
| QWIIC_CONNECTORJS                        | Mouse                    | [Buy](https://www.mouse.com/parts/QWIIC_CONNECTORJS)                                                 |
| SAMACSYS_PARTS_USB4110-GF-A              | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/SAMACSYS_PARTS_USB4110-GF-A)                    |
| SI1308EDL-T1-GE3                         | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/SI1308EDL-T1-GE3)                             |
| SJ                                       | GrabCAD                  | [Buy](https://www.grabcad.com/parts/SJ)                                                              |
| USBLC6-2SC6Y                             | SnapMagic                | [Buy](https://www.snapmagic.com/parts/USBLC6-2SC6Y)                                                  |
| W25Q512JVEIQ                             | SnapMagic                | [Buy](https://www.snapmagic.com/parts/W25Q512JVEIQ)                                                  |
| XC6220A331MR-G                           | Component Search Engine  | [Buy](https://www.components-search-engine.com/parts/XC6220A331MR-G)                                |


P.S on the routing part I had to leave 1 of the VBUS cables on the size of 1.27 due to it causing multiple errors with the design and routing process.


