# OpenBook eReader

This project is a minimalist eBook Reader called **OpenBook**, built around the ESP32-C6 platform. The device is contains:

  - **A 7.5-inch e-paper display**

  - **A Li-Po battery**

  - **USB-C charging**

  - **Navigation buttons**

The design focuses on energy efficiency and ease of use, featuring a simple interface managed via GPIOs. The primary goal is to provide an optimal e-reading experience with low power consumption and a comfortable display.

## System Overview

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



## Block Diagram

![IMAGE](https://github.com/user-attachments/assets/33e0b689-91f6-4aae-8e81-0fd5dd119592?raw=true)




## Bill of Materials:
| **Component** | **Purchase Link** | **Datasheet Link** |
|---------------|-------------------|---------------------|
| 112A-TAAR-R03 ATTEND | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/attend-technology/112A-TAAR-R03/17633923) | [Datasheet](https://www.snapeda.com/parts/112A-TAAR-R03/Attend/datasheet/) |
| BDS229G-TR | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/rohm-semiconductor/BDS229G-TR/3663792) | [Datasheet](https://fscdn.rohm.com/en/products/databook/datasheet/ic/power/voltage_detector/bds229g-e.pdf) |
| ESP32 WROVER BME680 Sensor | [Buy on Mouser](https://www.mouser.com/ProductDetail/Bosch-Sensortec/BME680) | [Datasheet](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme680-ds001.pdf) |
| LED CHG_LED | [Buy on Mouser](https://www.mouser.com/ProductDetail/Wurth-Elektronik/150060SS75000) | [Datasheet](https://www.we-online.com/components/products/datasheet/150060SS75000.pdf) |
| Condensator C0402 | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/murata-electronics/GRM155R71C104KA88D/675947) | [Datasheet](https://search.murata.co.jp/Ceramy/image/img/A01X/G101/ENG/GRM155R71C104KA88-01.pdf) |
| Condensator Tant | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/kemet/T491A106K016AT/2336183) | [Datasheet](https://search.kemet.com/download/datasheet/T491A106K016AT) |
| Q1 DMG2305UX-7 | [Buy on Mouser](https://www.mouser.com/ProductDetail/Diodes-Incorporated/DMG2305UX-7) | [Datasheet](https://www.diodes.com/assets/Datasheets/DMG2305UX.pdf) |
| RTC MODULE DS3231SN# | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/analog-devices-inc-maxim-integrated/DS3231SN/1197576) | [Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/DS3231.pdf) |
| ESP32 C6 WROOM-1-N8 | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-C6-WROOM-1-N8/17728866) | [Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-c6-wroom-1_wroom-1u_datasheet_en.pdf) |
| FH34SRJ-24S-0.5SH(99) | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/hirose-electric-co-ltd/FH34SRJ-24S-0-5SH-99/5132529) | [Datasheet](https://www.hirose.com/product/p/CL0580-1255-6-99) |
| MAX17048G+T10 | [Buy on Mouser](https://www.mouser.com/ProductDetail/Analog-Devices/MAX17048G+T10) | [Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/max17048-max17049.pdf) |
| MBR0530 Schottky Diode | [Buy on Mouser](https://www.mouser.com/ProductDetail/onsemi/MBR0530T1G) | [Datasheet](https://www.onsemi.com/pdf/datasheet/mbr0530t1-d.pdf) |
| ESP32 WROVER MCP73831 Power Management | [Buy on Adafruit](https://www.adafruit.com/product/4410) | [Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/20001984g.pdf) |
| PFMF.050.1 | [Buy on Mouser](https://www.mouser.com/ProductDetail/Littelfuse/PFMF050-1) | [Datasheet](https://www.littelfuse.com/~/media/electrical/datasheets/resettable-ptcs/littelfuse_ptc_pfmf_datasheet.pdf) |
| PGB1010603MR | [Buy on Mouser](https://www.mouser.com/ProductDetail/Littelfuse/PGB1010603MR) | [Datasheet](https://www.littelfuse.com/~/media/electrical/datasheets/esd_suppressors/littelfuse_esd_supressor_pulse_guard_pgb0603.pdf) |
| QWIIC_RIGHT_ANGLE CONNECTOR | [Buy on SparkFun](https://www.sparkfun.com/products/14427) | [Datasheet](https://www.jst-mfg.com/product/pdf/eng/eSR.pdf) |
| Rezistență R0402 | [Buy on Mouser](https://www.mouser.com/c/passive-components/resistors/?manu=Yageo%20Phycomp%7CYAGEO&resistance=10%20kOhms&package=%2Fcase%7C0402) | [Datasheet](https://www.yageo.com/upload/media/product/product_search/datasheet/cpr/yageo-rc_series_datasheet_2018.pdf) |
| SD0805S020S1R0 | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/littelfuse-inc/SD0805S020S1R0/736561) | [Datasheet](https://www.littelfuse.com/~/media/electrical/datasheets/resettable-ptcs/littelfuse_ptc_sd0805_series.pdf) |
| Si1308EDL-T1-GE3 MOSFET | [Buy on Mouser](https://www.mouser.com/ProductDetail/Vishay/SI1308EDL-T1-GE3) | [Datasheet](https://www.vishay.com/docs/63442/si1308edl.pdf) |
| USB4110-GF-A | [Buy on Mouser](https://www.mouser.com/ProductDetail/GCT/USB4110-GF-A) | [Datasheet](https://gct.co/drawings/usb4110.pdf) |
| USBLC6-2SC6Y | [Buy on Mouser](https://www.mouser.com/ProductDetail/STMicroelectronics/USBLC6-2SC6Y) | [Datasheet](https://www.st.com/resource/en/datasheet/usblc6-2sc6.pdf) |
| W25Q512JVEIQ | [Buy on Mouser](https://www.mouser.com/ProductDetail/Winbond/W25Q512JVEIQ) | [Datasheet](https://www.winbond.com/resource-files/w25q512jv%20revg%2011022019%20plus.pdf) |
| XC6220A331MR-G | [Buy on Digi-Key](https://www.digikey.com/en/products/detail/torex-semiconductor-ltd/XC6220A331MR-G/5027707) | [Datasheet](https://www.torexsemi.com/file/xc6220/XC6220.pdf) |
| 744043680 BOBINA | [Buy on Mouser](https://www.mouser.com/ProductDetail/Wurth-Elektronik/744043680) | [Datasheet](https://katalog.we-online.com/pbs/datasheet/744043680.pdf) |


## Power Supply & Battery Management

The system supports dual power sources:

- **USB-C (5V) input**
- **3.7V Li-Po battery (CELLEVIA LP584174, 1800mAh)**

Power is managed as follows:

- **MCP73831** – Charges the Li-Po battery when USB-C is connected
- **LDO Voltage Regulator** – Converts 5V USB input to 3.3V

##  Sensors & Real-Time Clock (RTC)

Connected via the I²C bus:

- **BME688** – Measures temperature, humidity, pressure, and VOCs
- **DS3231** – High-precision RTC with battery backup

Sensor readings are processed locally and can be used for both display and logging.

## E-Paper Display

The **7.5-inch E-Ink display** interfaces over SPI and is controlled using:

- `EPD_CS` – Chip Select  
- `EPD_DC` – Data/Command  
- `EPD_RST` – Reset  
- `EPD_BUSY` – Busy indicator

The display only consumes energy when refreshing. Once the image is rendered, it holds static content without any power draw — perfect for long battery life.

## The project realization process

- Firstly I built the schematic using the model given in OCW, for the PCB model I followed the scheme respecting the given parameters.
- I created the ground planes with the GND signal on the top and bottom.
- Autorooted the paths, made the cables 0.3mm and 1.5mm respectively. Here I had to keep 1 of the cables the default size of 1.27 because it would create a lot of errors. (AIRCABLE)
- Made the battery and screen 3d models respecting the given parameters. Rendernd all the 3d models and the whole of them combined.

