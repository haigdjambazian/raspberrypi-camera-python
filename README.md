# raspberrypi-camera-python
Using python and opencv on the raspberrypi
=========================================

Using: Raspberry Pi 3 Model B, MacBook Air (13-inch, Late 2010)

Create NOOBS microSD card
----------------------------

* Get latest NOOBS (NOOBS Lite) from: https://www.raspberrypi.org/downloads/noobs/  
I used NOOBS_lite_v1_9.zip, (old versions archived here: https://downloads.raspberrypi.org/NOOBS/images/)
* Unzip the NOOBS zip file.
* Copy the folder to the microSD card (used an microSD to SD adapter).

First boot
--------------

* Insert the microSD card.
* plug in the Mouse, Keyboard and hdmi.
* Plug in the power with microUSB to start the first boot process.
* A prompt appears to choose wifi network and enter password.
* A window will appear with a list of different operating systems.
* Choose Raspbian and click install, Raspian will install.
* When the installation is complete click "ok".
* Raspian GUI will start.

Installing RPi Camera
---------------------

* Connect camera with flex cable (with RPi off)
* Enable camera:
```
sudo raspi-config
```
* Select enable camera and hit Enter, Finish and it will reboot.
* To turn red camera LED off: add "disable_camera_led=1" in the /boot/config.txt
```
sudo nano /boot/config.txt
```

Install picamera for Raspbian
-----------------------------

Following: http://picamera.readthedocs.io/en/release-1.10/install3.html

Install python and picamera
---------------------------
```
sudo apt-get update
sudo apt-get install python3-picamera

sudo apt-get install python3-pip
pip-3.2 install --user "picamera[array]"
pip-3.2 install --user -U picamera
```

