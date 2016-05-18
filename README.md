Raspberry Pi ESP8266 Wifi Driver
======
####A driver to use an ESP8266 module for full GPIO wifi on a Raspberry Pi.

####For more information visit [http://oshlab.com/esp8266-raspberry-pi-gpio-wifi/](http://oshlab.com/esp8266-raspberry-pi-gpio-wifi/)


This is a driver for using an ESP8266 wifi module for wifi on the Raspberry Pi. To use this, you need an ESP-12E or ESP12F module. The ESP-12F is recommended. An install script is included to completly setup everything for the module. This is based heavely on [RPi WiFi](https://hackaday.io/project/8678-rpi-wifi) on Hackaday.io. I have made some changes to the Makefile so it works with the latest kernel. I also added a startup script that is automatically installed to handle the GPIO in order to activate the module. I also made the setup process much easier. 

First, wire up the ESP-12F like this. 

![](http://oshlab.com/wp-content/uploads/2016/05/ESP-Pi-WiFi-wiring-1024x536.jpg)

SSH into your Raspberry Pi and enter the following commands.

`cd ~`
`git clone https://github.com/oshlab/esp8089.git`
`cd esp8089`
`sudo sh install`

This is going to take a while.

When that is done, reboot your Pi.

`sudo reboot`

After reboot, the ESP8266 module should activate. You can do a quick scan to make sure it is working.

`sudo iwlist scan`

Now it will work just like any other WIFI module. Cheers. 