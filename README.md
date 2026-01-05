# PCB-LogicShifterUnit
This logic level shifter has the same shape as the M5Stack Unit and can be used to connect the M5Stack Unit or M5Stack Controller (Core, Atom, etc) to an Arduino.

<img width="1723" height="892" alt="logicshifterunit" src="https://github.com/user-attachments/assets/e3cacbac-9177-4f88-9070-0103ed1bdf89" />

## Specification
The side marked "LV 3.3V" allows you to solder 2mm pitch 4-pin connectors. This includes Grove connectors and PH connectors. The signal voltage is 3.3V. Please note that the power supply voltage is 5V.

The side marked "HV 5V" allows you to solder 2.54mm pitch 4-pin connectors. This includes common pin headers and XH connectors. The signal voltage is 5V.

There is no specification for the direction of the power supply or signal. Signals are pulled up. Analog signals cannot be handled.

## Pinout Tips
| LV-Side Device | HV-Side A | HV-Side B |
| ---- | ---- | ---- |
| M5Stack Controller & Unit (I2C) | SDA | SCL |
| M5Stack Controller (UART) | LV:TxD HV:RxD *1 | LV:RxD HV:TxD *1 |
| M5Stack Unit (UART) | LV:RxD HV:TxD *1 | LV:TxD HV:RxD *1 |
| M5Stack Controller & Unit (GPIO) | *2 | *2 |

- *1: In the case of LV:TxD HV:RxD, connect the RxD pin of the Arduino or any microcontroller to HV-Side A, and vice versa.
- *2: For Controller, please check the your source code, and for Unit, please check the product page.
