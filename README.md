## Smart-Modular-RGBW-Aquarium-Lamp
An OpenSource project about a RGBW Lamp for Aquariums.


<div align="center">
      <a href="https://www.youtube.com/watch?v=695nHi4XT3Q">
         <img src="https://img.youtube.com/vi/695nHi4XT3Q/0.jpg" 
           style="width:75%;">
      </a>
</div>


The idea of a RGBW lamp for aquariums stems from the idea of having an open-source lamp, which has the characteristics of being highly feature-rich due to its open-source hardware and software but at the same time easily repairable or interchangeable due to its modularity at very low cost. The lamp can be controlled via Bluetooth via your smartphone and allows you to manage the light intensity separately, so that you can have the lighting effect you like best and bring out the colours of the aquarium. In addition, you can set on and off times for the lamp with fading time to simulate sunrise and sunset. Finally, it is possible to monitor the aquarium water temperature via sensor.



## APPLICATIONS TARGETED:

- Aquariums Fresh/Salt Water
- Aquaponics
- Terrariums
- Plants Growth

## Due to its modularity, the lamp consists of five components listed below:

- LED-Drivers PCB x 4
- ESP32 PCB Controller x 1
- Central Board x 1
- LED-Boards x 4
- Interface Board (between Main Board and LED-Boards) x 1

## OTHER REQUIREMENTS:

- Power Supplier 24V/3A
- 3D-Printed Case
- M3 Inserts x 8
- Aluminium Round Bar 10mm x 1

## EQUIPMENT USED:
- MiniWare MHP30
- Miniware T80 IronSolder
- PLA 1.75mm Wood
- Bambulab A1 Mini


## My Vision
I hope this lamp it's a starting point to an open source and community developed project! I will updates this projects with new features both hardware and Software side! If anyone is interested to cooperate with me on this project is welcome!

This is the first Aquarium Open-Source Project!

<p align="center">
    <img width="30%" src="/images/IMG20240515114320.jpg">
</p>

# The Hardware
<p align="center">
      <a href="https://www.pcbway.com">
    <img width="50%" src="/images/FJKDQBULVZ9DD6S.webp">
      </a>
</p>
I wanted to make PCBs as small as possible, modular and high quality. That is why I relied on the quality, reliability and efficiency of PCBWay, a leading PCB fabrication company. I was amazed by the PCBWay customer service, they answered all my questions by mail, and very quickly. The price is very competitive and the production and delivery times are very fast, impeccable service.

#### The lamp is composed by 4 main PCB Boards:
- LED-Driver PCB
- ESP32 Micro-controller Board
- Central Board
- LED-Boards
- Temperature Sensor


##  LED-Driver PCB
<p align="center">
    <img width="30%" src="/images/IMG_20240515_111533.jpg">
</p>
The LED-driver is an essential component for the correct functioning of LEDs. The lamp is equipped with 4 led-drivers that allow 4-channels to be managed separately to set the light intensity. The modularity allows the PCB to be replaced for failure or to increase light output at a very low cost. This makes it possible to have a highly customisable lamp depending on the field of use.


## ESP32 Micro-controller Board
<p align="center">
    <img width="30%" src="/images/IMG_20240515_111744.jpg">
</p>
The ESP32 is the micro-control which allow, through the Bluetooth protocol, to control, via smartphone, the intensity brightness of the 4-channels, set the on/off time with sunrise/sunset effects and control the temperature of the water in the aquarium or plants. The PCB relating to the ESP32 is also modular as it allows to be replaced easily and at low cost due to malfunctions or failures of the microcontroller.


## Central Board
<p align="center">
    <img width="30%" src="/images/IMG_20240515_111858.jpg">
</p>
The central-board is the core of the modularity. On the central-board there are the electronics components that allows to manage the power-supply for the Micro-Controller and the LED-Drivers but also to connect the water temperature sensor to monitoring the aquarium water.

## LED-Boards
<p align="center">
    <img width="30%" src="/images/IMG_20240515_112120.jpg">
</p>
The LED-Boards allows to have 7 leds for each board, for a total of 28 leds. The modularity of the LED-Boards allows to use different type of leds i.e. 1W or 3W, so potentially upto 84W and 4500 lumens , with optimal heat dissipations techniques.

## Temperature Sensor
<p align="center">
    <img width="30%" src="/images/IMG_20240515_112855.jpg">
</p>
The aquarium lamp is provided of a Temperature Sensor that allows to monitor, even from remote, the water temperature of the aquarium. In addition, it's possible to set trigger events notifications for anomalies/warnings i.e. when the water temperature is greater than 30°.


# THE SOFTWARE
<p align="center">
    <img width="30%" src="/images/IMG_20240515_123100.jpg">    <img width="30%" src="/images/IMG_20240515_132731.jpg">
</p>
Basically, the logic execution of the aquarium lamp is performed by the ESP32 microcontroller software, while the controlling/managing of the lamp is done by the android application. In addition, it is possible to monitoring from remote some parameters like water temperature with historical chart, thanks to the integrity of Blynk IoT Cloud Platform.

#### In this chapter will be explained the main features of the Aquarium Lamp, dividing it in 3 sections:

- ESP32 Firmware
- Android Application
- Blynk IoT Remote Control

## ESP32 Firmware
The ESP32 Firmware is the core of the aquarium lamp, where all the logic of the functions are executed.

#### The main purposes of the ESP32 Firmware are:

- Handle the WiFi/Bluetooth connection with application to receive commands.
- Set the brightness intensity of the LEDs.
- Set the scheduling time to Turn ON/OFF the lamp with sunset/sunrise effects.
- Display the current Power of the lamp.
- Monitor the Water Temperature.
- Handle the Blynk IoT Connection to monitor/set remotely some parameters.
- Get info about the IP Address, Firmware Version or Current Time.
- Update the firmware via OTA.

## Android Application - the First Screen
<p align="center">
    <img width="30%" src="/images/IMG_20240515_122922.jpg">
</p>
The Android Application aims is to control via Bluetooth the Aquarium Lamp.
In this section it will be explained the main features of the application and how to use it!
In this screen will be displayed all the bluetooth lamp associated with the smartphone, click on one of it will open the main screen to controll the selected lamp.

## The Main Screen
<p align="center">
    <img width="30%" src="/images/IMG_20240515_123100.jpg">
</p>
In the main screen is possible to set the brightness intensity of the lamp with power, visualize the current water temperature of the aquarium, the scheduled time and the current total power used.
In addition, a floating button allows to open a menu to configure or execute some settings.

## The Floating Button Menu
<p align="center">
    <img width="30%" src="/images/IMG_20240515_123047.jpg">
</p>
Clicking on the Floating Button will open a menu that allows to enter in 3 main page:


- Scheduling page
<p align="center">
    <img width="30%" src="/images/IMG_20240515_122954.jpg">
</p>
On this page is possible to set the time to turn ON/OFF the lamp. On the left, you can set the time to turn on the lamp setting the hours and the minutes, the same is possible with the right gauge to turn off the lamp. Indeed, varing the value in the green gauge is possbile to set the minutes of the fade to simulate the sunset/sunrise effect.

To correctly set the scheduling mode, you need to set the switch button to "AUTO" and click on "SAVE AND EXIT". When the lamp is setted to scheduling mode, it is not possible anymore to manually set the intensity brightness on The Main Screen.

At this point, when the internal clock matches the scheduled time, the lamp will turn on/off with the fade effect selected until the brightness reaches the manually intensity previously configured.



- Info Page
<p align="center">
    <img width="30%" src="/images/IMG_20240515_123032.jpg">
</p>
In the current page is possible to get info about the IP Address of the device connected to the WiFi, check if the current time of the lamp is synced with the clock and check the firmware version of the lamp.
In addition, is possible to update the firmware of the lamp via OTA. To do this, click on the "Update Firmware" button. At this point in the wifi settings of the smartphone/PC it will be diplayed a new wifi device called "LAMP_updater" use the password "aquariumlife" to connect to it.
Open now a browser and digit the address 192.168.4.1, the OTA page will be showed, now click on "Select File" and select the Firmware.bin file downloaded by GitHub and done.


## Blynk IoT Remote Control
<p align="center">
    <img width="30%" src="/images/IMG_20240515_132731.jpg">
</p>
The Blynk IoT Cloud allows to monitor from remote, when you are far from home, some parameters of the lamp like the aquarium water tempearture, allowing even to set some trigger events like temperature anomalies with notification on app.

DashBoard (click to see image)


# 3D Printed Case
<p align="center">
    <img width="30%" src="/images/IMG_20240515_111055.jpg">
</p>
The case of the Aquarium lamp has been designed with SolidWorks and printed with the Bambulab A1 Mini.

The main parts are basically 4:

- The case to store the electronics.
- The cover to close the case and hold the lamp with a bracket
- Wings/Deflectors to improve the reflections of the lights
- A white light diffuser to make the light homogeneous.

# How Can I Have This Lamp?
Basically you have two options:

- Downloading PCB Gerbers and have them produced by a PCB company such as PCBWay.
- Buying directly the Lamp from my store, helping me to support and continue to develop the project with new features and updates.

# General Q.A.
1. How can i pair the lamp with the phone?
   - Go to the settings of your phone and pair from there the lamp device, once done open the app and start the scanning process.
2. How can i update the firmware?
   - Open the app and go to "info" (the green icon on the main menu), press "UPDATE FIRMWARE". The device will be setted-up in AP mode with SSID "LAMP_updater" and type the password "aquariumlife". Once connected open a tab on browser and type the following address [192.168.4.1/update](http://192.168.4.1/update) , now "Select file" and choose the .bin you downloaded, the process will start automatically.

