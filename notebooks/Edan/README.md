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

# 03/27/2024
### Control Unit Schematic and PCB for the first PCB order
![](Control_Unit_Schematic2.png)
![](Control_Unit_PCB2.png)

# 04/07/2024
### Data Collection with ESP32 Devboard and IMU Breakoutboard
We have been struggling to use the ESP32 Devboard, but found that the one we were using was broken and were able to use a new one to connect to the IMU breakout board. Below is the setup we used as well as a sample of the data we collected.
![](devboard_breakout_setup.jpg)
![](sample_data.jpg)<br />
The data has a substantial amount of noise so it will be important for us to use filtering techniques to clean the data.

# 04/11/2024
### Final Schematic/PCB
![](Final_Schematic.pdf)
![](Final_PCB.png)
### Multiplie Addresses on I2C
We were able to connect two sensors on the I2C bus by changing the address of one and accounting for it in software. We now need to connect the others by figuring out how to add aditional I2C pins on the esp32 through software.
