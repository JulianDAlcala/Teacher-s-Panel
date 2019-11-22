# TEACHER´S PANEL
A repository for a attention panel of students to help communicate with teachers in counseling schedule.
* Watch the Youtube video :
# This repository contents:

* Source code
* Data files
* Dev script

# **Hardward Requirements:**

* A Raspberry py 3 [https://www.raspberrypi.org/products/raspberry-pi-3-model-b/]
* 2 module Nodemcu ESP8266 [https://naylampmechatronics.com/espressif-esp/153-nodemcu-esp8266.html]
* A Touch screen 3.5" for raspberry py 3 [http://www.lcdwiki.com/3.5inch_RPi_Display]
* A servomotor to 5V [http://www.ee.ic.ac.uk/pcheung/teaching/DE1_EE/stores/sg90_datasheet.pdf]

# **Software Requirements:**

* Ubuntu 16.04
* Python 2.7 necessary libraries(mqtt,flask,xlrd)

# **How to install**

It´s neccesary to install the libraries as follows

* To install mqtt:
``` sh 
sudo apt install -y mosquitto mosquitto-clients 
```
This library is needed because it is a lightweight open network protocol that usually runs over tcp / ip which allows sending and receiving data via Wi-Fi and is perfect for IoT applications.

* to install paho-mqtt
``` sh 
pip install paho-mqtt
```
that library helps to implement versions 3.1 and 3.1.1 of the MQTT protocol.
* to install fask: 
``` sh 
sudo pip install flask
```
This library is where you can use the rasberry pi 3 to host the website i.e, the server where all the information will go.

* to install xlrd: 
``` sh
pip install xlrd"
```
With this library you will be able to link the excel documents with the website and thus be able to read the information files that will be run.

# Connection between the rasberry pi to touch screen 3.5" 

Usually when you use the rasberry pi you connect way to hdmi with a monitor. In this case, you use a touch screen 3.5" directly connect to raspberry pinout, so you need to put some commands.
``` sh
sudo rm -rf LCD-show 

git clone https://github.com/goodtft/LCD-show.git 

chmod -R 755 LCD-show 

cd LCD-show/

sudo ./LCD35-show
```
In the last line this 35 indicates the size of touch screen that is so important because if you will to work with another touch screen, you will need another commands.

If you want to come back to work since the monitor , just need to put the next commands in the terminal.

``` sh
chmod -R 755 LCD-show 

cd LCD-show/ 


sudo ./LCD-hdmi
```
