# 02/21/2024
### Pins we will need to use on the ESP32-S3-WROOM-1
* Power -> 3V3
* Ground -> GND
* Enable -> EN
* Strappint Pins -> GPIO0, GPIO3, GPIO45, GPIO 46
* USB -> GPIO 19, 20
* JTAG -> GPIO39, GPIO40, GPRIO41, GPIO42
* UART -> GPIO43, GPIO44
* SPI -> GPIO10, GPIO11, GPIO12, GPIO13
* LEDs -> GPIO1, GPIO2

# 03/19/2024
### Control Unit Schematic and PCB for the first PCB order
![](Control_Unit_Schematic1.png)
![](Control_Unit_PCB1.png)

# 03/25/2024
### Voltage Regulator Recalculations
Our voltage regulator uses resistor values that we do not have provided, so we used the equation Vout = 1.25*(1+R1/R2) + R2*50e-6 to get new resistor values. The new resistor values to get each voltage are:
* 3.3V -> R1 = 1500Ohms (1.5kOhms), R2 = 2330Oms (1kOhm + 1kOhm + 330Ohms)
* 1.8V -> R1 = 5100Ohms (5.1kOhms), R2 = 1330Ohms (1kOhm + 330Ohms)
