![weekone](uploads/3f6d00a4eb90633511fdadfa3d804e1a/weekone.png)

# REFIXING THE PH-SENSOR AND CONNECTING THE WHOLE DEVICE 

We began the first lecture of the week by reviewing our pH sensor from the previous week and examining the bugs in our code. The teacher explained the reasons behind the issues we encountered with the pH sensor and demonstrated possible problems on the board shown below. 

![IMG_5657](/uploads/dfdb6a39a50631d51b1f0e1c5e94b360/IMG_5657.jpeg)

He drew and explain on the board that the Arduino operates at 5 volts, while the ESP32 operates at 3.3 volts, which means that to connect the two safely, we need to convert the 5V signals from the Arduino down to 3.3V before they reach the ESP32. He said directly sending a 5V signal to the ESP32 could damage its input pins, as they are designed to handle only up to 3.3V. To achieve this voltage conversion, we can use a voltage divider circuit with two resistors. Typically, a 10kΩ resistor and a 20kΩ resistor are used in series to create the necessary drop in voltage. In this setup, the 5V signal from the Arduino goes through the resistors, and the junction between the two resistors provides an output of approximately 3.3V, which is safe for the ESP32. This method, is known as a voltage divider. Additionally, He further explained that this method allows smooth communication without risking the integrity of the ESP32, and that the resistors work together to reduce the voltage proportionally, protecting the ESP32 from potential damage.

In our group, we divided the tasks. Some students focused on obtaining the two resistors needed to adjust the ESP32 and recalibrate the pH sensor, while others worked on the front end of the device. I was working with the Node.js and HTML files, where I set up data reception from MQTT and TTN, allowing us to display the information on our dashboard within the user interface.

# RECONNECTING THE WHOLE DEVICES

Our group leader in collaboration with other students fixed the device by connecting the PH sensor, Temperature Sensor, Meter Sensor, with the GPS and LoRaWAN Arduino network from the previous weeks to see if they are working by Using node js via matt to get data from the things network. Then fetching the data to the DATABASE so that I can utilise them by utilising it or receive data from MTTQ and TTN and display it on our dashboard in our user interface 

The group leader, in collaboration with other students, reconnected the pH sensor, temperature sensor, and meter sensor to the GPS and LoRaWAN Arduino network from previous weeks to test their functionality. They used Node.js through MQTT to retrieve data from The Things Network (TTN), storing this data in the database. This setup allowed me to access and utilise the data from MQTT and TTN, displaying it on our dashboard in the user interface.

![IMG_5665](/uploads/37c0453488274c5e70704a79c2fa45dd/IMG_5665.jpeg)

## RETRIEVING DATA TO THE USER INTERFACE

After setting up the device, I checked with my group members to confirm if it was working properly and if data was appearing on The Things Network. I was specifically looking for data such as temperature, latitude, altitude, and pH levels to ensure the setup was transmitting as expected. Once the data appeared, I was able to run the Node.js code provided by Arthur and Andre. My task was to modify the Node.js and HTML files to pull data from both the MQTT and The Things Network, displaying it on the dashboard in our user interface.

The first step I took was in Node.js, I created functions to retrieve data from both sources. Use database queries to pull stored data and MQTT subscriptions to receive real-time data from The Things Network. I Formatted the retrieved data to be ready for display, organising it into objects or JSON. Then  modifying the HTML file to include elements where data will be displayed by using JavaScript to dynamically update these elements with the Node.js data. Then I ran the Node. js file on my terminal and i got the displayed in real-time on the user interface as shown below. 

![real-LifeData](/uploads/e79e1088552e0bf9cab6e2b87d35b44f/real-LifeData.png)

On the live data dashboard, you can see the current location of our device displayed on the map. Below the map, various parameters, values, and timestamps are shown, providing real-time information. I will go into more detail about these metrics and their significance later after the final prototype. 

# FINAL DASHBOARD PROTOTYPE

Today Tuesday, November 5th, I focused on finalising our dashboard prototype. The task was divided among the group. Some students worked on the backend, while others handled the hardware, including sensors, GPS, and LoRaWAN. My role was to enhance the Node.js, CSS, and index.html code to create a more interactive user interface that would displays the live data we’ve been working on over the past two weeks.

#### The Improvement

I made improvement on our final user interface dashboard I created earlier as you can see on the photo above. Today the first thing I thought of was ‘us’, my team mates and I as a group. I also asked myself how will the users recognise who created of this user interface? That was when I realised we have a name and a logo that bond us together as a group. So, I implement the Logo on the left top corner of the page, with HTML, CSS and an Image which was stored on the public folder. The next step I took was to check the prototype we created in the last module in Spain, to see if it match the current dashboard that I am creating. I saw that the footer was missing. I created the footer with also HTML, CSS and some icons which I also stored in images in the public folder. Lastly I explained with words on the footer what we aim to display on our dashboard and our goal as team NEXUS

![dashBoard](/uploads/26ab1d0fb687e2e1e981d053c0888603/dashBoard.jpeg)

The map on the dashboard is interactive. On the map you can see the topographic view, which represent the area where data is being collected here in Hagenberg. The blue location pin on the map indicates the exact spot where the IoT device is located. This marker provides a quick visual reference to the location of the data source.  Below the map, there is a data table with three columns- "Parameter," "Value," and "Timestamp." The table lists various parameters monitored by the IoT device, along with their current values and the timestamp for each data point. Under the parameters we have 

- **Device ID**: "Nexus-Lowa," which is our unique name for the IoT device.

- **Latitude and Longitude**: Which displays the geographical coordinates (48.3676897281538, 14.5125124865241) of our device’s location.
- **Altitude**: Which shows "270," in meters at that time, indicating the elevation of the device.
- **Temperature**: Which was currently showing "N/A,"  meaning that temperature data was unavailable because it takes more time to load.
- **pH: Shows** "0.15," which was a measurement of the water’s pH level, that came with the pH. 

At the bottom of the page, I added a footer with additional information about Nexus, my group which explains our focus on monitoring, managing, and controlling invasive species with a data-driven approach to protect the ecosystem. Lastly, below the description, there are social media icons for Facebook, Twitter, LinkedIn, and Youtube, allowing users to connect with us on these platforms.

#### Final Adjustment

On October 6th, our group focused on creating our final presentation and finalising our prototypes, including the IoT device, backend, and frontend for the module. We divided the tasks accordingly. Some students concentrated on the IoT device and sensors, others on the backend, and I focused on the frontend development. 

I picked up from where I left off yesterday. My first step was to revisit the prototype we created during the UX Design module in Spain. While reviewing it, I noticed that the map displaying our device's location was larger in the prototype compared to the current map on our live web application. I inspected the map on the dashboard to check its current size and began editing it, increasing the width to 120% and the height to 450px. I also adjusted its position slightly to the right by 77px. After confirming that it fit well, I asked my group mates if they preferred this larger map over the smaller version, and they agreed with the change I made as shown below. 

![finalDashbaord](/uploads/cb6edc4f6a9c1b9dabf6f33a8e27fe45/finalDashbaord.png)

We noticed that the TDS sensor data was missing from our dashboard. Arthur was already working on adding it, and I was working on it as well. Since we had similar code in the Node.js file for the pH, temperature, altitude, longitude, and latitude data, I simply duplicated and modified this code for the TDS sensor. After testing, I saw the TDS data displayed on the dashboard, functioning as expected. When I went back to update my team, I realized Arthur had also successfully implemented it, resulting in us having two separate pieces of code for TDS data, both working perfectly.

# FINAL PRESENTATION

[Final Presentation](https://hogeschoolpxl-my.sharepoint.com/:p:/r/personal/12200443_student_pxl_be/_layouts/15/Doc.aspx?sourcedoc=%7B1ded0e7a-341d-47e7-9a68-1506bac2aab1%7D&action=default&wdLOR=c2EA4A440-7A8D-9044-9DFF-31C4F9F3E072&CID=269b18b5-8e60-4166-bb64-751c99368197&_SRM=2%3AE%3A11&file=IoT.pptx)

![pre](/uploads/7720fd33e7b40c6403528ab4da69be57/pre.jpeg)

On Thursday, 7th of November, we delivered our final presentation in the IoT module. On the final we showcased our completed project device and all key deliverables. We also divided the presentation slides among ourselves. Tiaan, as the group leader, introduced the project and provided an overview of our objectives. Andre presented the technical overview, while Tiaan also explained the sensor integration and described the various hardware prototypes we developed and refined throughout the module. Carli discussed the final adjustments made to the project. Arthur covered the challenges we faced, along with reflections and next steps. I discussed the current status of the project and provided a detailed explanation of how our device operates on the dashboard, including an overview of the data it provides.