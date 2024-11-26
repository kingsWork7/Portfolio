![weekone](uploads/3f6d00a4eb90633511fdadfa3d804e1a/weekone.png)

# INTRODUCTION 

On the 21st of October, we kick-started this module as the University of Applied Sciences Upper Austria, Campus Hagenberg. The teacher of this module introduced himself to us, his name is Volker Christian. He is a Professor for Multimedia Programming, He has various degrees in Theoretical particle physics (subnuclear), Pervasive computing, Electrical engineering. He likes Swimming, physics, and all aspects of computer and network sciences. 

## LoRa, LoRaWAN and The Things Network

### LoRa, LoRaWAN
In our first lecture, we were informed by Volker that LoRa and LoRaWAN are the primary networks we will be using and focusing on in this module. He gave us an insightful lecture on LoRa (Long Range) and LoRaWAN (Long Range Wide Area Network) technologies. Fromm this lecture I learnt that LoRa is a wireless technology made for communicating over long distances, providing energy efficient, low power connectivity across distances up to 15 kilometers in rural areas and several kilometers in urban environments. While LoRaWAN is the communication protocol and system structure designed for LoRa, enabling it to support large-scale IoT deployments by efficiently managing data from thousands of devices. He went for to inform us that together, LoRa and LoRaWAN are ideal for applications where low power consumption and long battery life are critical, such as using sensors for environmental monitoring like the Haartbeesport Dam in South Africa, smart agriculture, asset tracking, and smart city infrastructure. These networks allow devices to transmit small amounts of data over extended distances without requiring high power, making them a cornerstone in developing scalable IoT solutions.

![loRa](/uploads/008d38513e7f2def700db5e8b26ee9a3/loRa.png)

### Comparing LoRa, WiFi, BLE and Cellular

In this lecture, I also gained a broad understanding of the differences between WiFi, LoRa, and Cellular Networks through comparison. As earlier explained that Lora was designed for long range, low-power communication, for IoT applications that require low data rates over large distances, the other networks are designed differently. For Example Wifi which is widely known was designed with high speed, medium-range network suited for high data transfer within limited areas (like homes or offices), consuming moderate to high power, is not ideal for low power IoT devices. While BLE is a short range, low-power communication mainly for personal device connections. Although He further explained  that Cellular Network also has Long range like LoRa, but they uses high-power networks providing wide area coverage and high data rates, suitable for applications which is not require in Lora. That is why LoRaWAN is very important for our Project. 

![loRaWifi](/uploads/afb786ecc57b1a3c580e85c254418bca/loRaWifi.png)

He skipped a lot of the presentation and went straight to the most useful information that will benefit us in the module for our project.  He went further to talk about the Architecture of a typical LoRaWAN Deployment. Which works End to End from the Server to the internet and also from the Server to MQTT broker then to our mobile phones Or from the server to HTTP server and then to our mobile tablets. From the other End, the internet connects to the Gateway that then connects to our home devices like the Air conditions, Water meter, Alarms and Lights. 

### Class - Work

To start up the physical part of this module, we were giving a box containing technological items. From the box we were asked to use microcontrollers like the ESP32 Mini d1, different types of sensors, bread boards, LEDs and some jumper wires (Male to male, male to female and female and Female). 

#### Task 

**Connects the Microcontroller and sensor to your computer using ARDUINO IDE to make the LED light blink.**

![IMG_4973](/uploads/0695a4be12202b25566cde59d4e440e6/IMG_4973.jpeg) 

**Process**

I did quite a similar project last semester by using Arduino UNO, sensors, bread boards, LEDs and some jumper wires (Male to male, male to female and female and Female), to make a smart street light. So the first step I took was to connect the ESP32 mini D1 to the Sensor without the bread board. Then I followed a tutorial page online that shows the PIN number of the ESP32 WROOM. 

<img src="/uploads/151f3b49a937352d2ba691ff6a14a17a/esp32.jpeg" width="200" length="120">

<img src="/uploads/fff118b4235af10946d8e275f23d48b1/eps72.jpeg" width="210" length="120">

<img src="/uploads/17261d4dc1057da1cb753c81efa3d0e1/all.jpeg" width="230" length="150" >

I connected the LEDs to the breadboard, using jumper wires to link the LED to the appropriate PIN on the ESP32 Mini D1. Then, I opened the Arduino IDE, created a new sketch, and selected the correct port for the ESP32. After uploading the code, the LED turned on. On my second attempt, I modified the code to make the LED blink. I changed the PIN number, adjusted the HIGH and LOW states, and set the interval for the LED to blink at specific intervals.

![cc](/uploads/9c25bbd31866df713490c01d1629a333/cc.jpg)

# The Things Network (TTN)

In the second lecture of the week, we were introduced to The Things Network. Building on what we learned about LoRa and LoRaWAN in the first lecture, this session focused on how LoRa and LoRaWAN connect with IoT devices. I learned that The Things Network was designed to provide LoRaWAN connectivity for IoT devices.

![TTN](/uploads/6b68ad1980292c07cbe0006d3e04d319/TTN.png)

One of our main project objective from the stakeholders from Central for biological Control was to detect the water hyacinth itself or macrophytes on water and detecting the floating species and also tracking its motion.  To detect and track these invasive species requires sensors, and The Things Network connects with LoRaWAN to enable sensors and devices to communicate with cloud-based applications efficiently which will help us details the movement of these Invasive plants and macrophytes. 

To make this work The Things Network utilizes the LoRaWAN protocol to create a link between IoT sensors, devices, and cloud-based applications, enabling efficient, low-power, long range communication as shown picture below in some areas in AUSTRIA

![TTNa](/uploads/81d3e564045e9583beb140b190181b2a/TTNa.png)

## Creating Our First LoRaWAN Application

On the third lecture, we were asked by the teacher to register The Things Networks. He gave us guidelines on how to register it and create an application with a name that represents our hardware device that will show on the Things Network interface, to show live data of the LoRaWAN connection. Before registering the Things Network with our group name. He told us to connect LoRaWAN Hardware, the EPS32 Microcontroller to the breadboard with some jumper wires and LEDs, and also Add the LoRaWAN to the breadboard as shown in the picture below

![loraconnection](/uploads/cef676bc29f3f883345faf634c30fd14/loraconnection.jpeg)

After connecting our LoRaWAN device on the breadboard. As a group, we registered The Things Network with an email and password and on The Things Network server we named our End device  “Nexus lowra”.  We were given a link on discord to a C++ code on GitHub. This code is to show all the Data that our device we connected to the LoraWAN is outputting on the Application overview. There is also a live data page where all data from our device will be shown. Other import pages on The things Network are Payload formatters which is essential for decoding and encoding data sent between IoT devices and applications, Integrations page which allow smooth connection between IoT devices and external applications or services, the collaborator page allow us as a team of multiple users to manage and access our project, enabling team collaboration on our device configurations, data management, and network monitoring. We also have a page for API Key to secure access control and allow us as users to interact with our devices and data. We take the API Key after registration and add it to our code in C++ to give us access to data from our connected device.  Lastly there is a general settings page in The Things Network which enables users to set up essential project information like device names (Nexus Lowra) , descriptions, and network settings, making the IoT setup easier to organize and customize. 

![loraAPI](/uploads/88864386d0c26c5f01e167d711bb1697/loraAPI.png)

# The Things Network (TTN) and GPS Connection

On the fourth and last lecture of the week, Friday 25th October. We were asked by our teacher to connect a GPS to our LoRaWAN network and display it on The Things Cloud. We were also provided a code in discord by the teacher, that enables our IoT device connection collect GPS location data and send it over the LoRaWAN network. Getting this setup was very difficult at first, with a lot of questions to the teacher, online google and feedback. we manage to start the setup. At first, we connected the GPS to the LoRaWAN and took the device to the window to help it get a better signal, we then waited for 5 minutes to see of a light will flash from the LoRaWAN device. 

![loRaWAN](/uploads/a86dc1aba9e5d8991c0d6a3633d9b246/loRaWAN.jpg)

In this setup, the program starts the GPS module to gather location coordinates like latitude, longitude, altitude, and speed. It then changes these coordinates into a format that meets the payload criteria of LoRaWAN. The data is encoded and packed into a payload to reduce transmission size, ensuring efficient and low power communication. Then the LoRaWAN module connects to a gateway and sends the GPS data to the network at set times or when certain conditions are met. Finally the GPS data from our device is displayed in the "Live Data" section on The Things Network we created. When the GPS device sends its location data (e.g latitude, longitude, and altitude) through our LoRaWAN device, this data appears in real time on our live data platform as shown below. 

![LoraDATA](/uploads/6b2bada604389c00d09d65b04fb22997/LoraDATA.png)