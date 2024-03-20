# Kaylan's Lab Notebook

# 2024-02-14 - Discussion with TA Sanjana Pingali

Sanjana gave us the idea to have LEDs on the front of the wearable for visibility for drivers in front of the user. Additionally we were told we might have to design and create our own breakout board for the IMUs so I will be looking into that in the near future.

# 2024-02-19 - Proposal

We are currently working on the proposal rewrite and we decided on removing the back shoulder LEDs and running a longer strip from the wrists up to the shoulder area and then wrapping it above the shoulder to the upper chest. This way we can reduce the load on the battery as well as integrating some front facing lights as discussed with our TA. Visual aid for reference:

![](visual_aid.jpg)

I am currently looking into creating a schematic for the IMU breakout board and found that the schematic for the breakout board we were planning on using (Adafruit LSM9DS1 Accelerometer + Gyro + Magnetometer 9-DOF Breakout) has their [schematic](https://learn.adafruit.com/adafruit-lsm9ds1-accelerometer-plus-gyro-plus-magnetometer-9-dof-breakout/downloads) published online. We will likely use this as a reference if we are asked to manufacture the breakout board from scratch. 

# 2024-02-27 - Design Review

I've been thinking about the physical aspect of the project and how we will incorporate the LEDs and electronic components into the wearable. We discussed the idea that the electronics need to be removable so that the user can wash the jacket. Therefore the tentative plan for the physcial design will be the LEDs, IMU will be attached via velcro to the sleeves, PCB and battery in the inner pockets. 

# 2024-03-1 - PCB Review (IMU changes)

I've been working on the IMU schematic and found that the original IMU we wanted to work with (LSM9DS1) is not in stock anymore so we decided to switch to the ICM-20948 IMU. The TA at the PCB review suggested we switch from the SPI protocol to the I2C protocol for the IMU so I have made the necessary changes to the schematic. I'm including the INT and SD0/AD0 signals in the case that we need them. The schematic will be submitted for the first round PCB orders.

![](IMU_schematic.png)
