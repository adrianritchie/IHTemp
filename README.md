# IHTemp
Temperature monitor using ESP8266 (Wemos D1 Mini R2), DS18B20 and Blynk

# Schematic
![schematic](docs/schematic.png)

#Setup
When the device is powered by USB, the ESP8266 will attempt to connect to a WiFi network.  If it is unable to connection to a network that it was previously connected to, it will create a local access point (AutoConnectAP).  Connecting a mobile phone to this AP will open a congifuration page in which the device can be connected to an existing WiFi network.  At this point, the Blynk settings can also be configured:

* Blynk server;
* Blynk auth token;
* Virtual Pin number of the device, for use in Blynk.

Following configuration, the device will restart, connect to the configured WiFi network and begin logging the temperature to the Blynk server using the specifid Blynk token and virual pin.

#Resetting
If it becomes necessary to reset the configuration of the device, this can be acheived using the reset button.  To do this holder down the reset button attahced to pin D5 and then power cycle the device.  Continue holding the button until the LED starts blinking once a second.  Release the reset button.  The device will automatically restart and will need to be reconfigured using the AutoConnectAP in the setup instructions above. 
