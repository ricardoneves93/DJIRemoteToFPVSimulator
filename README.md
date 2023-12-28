# DJIRemoteToFPVSimulator

If you want to use the <b>DJI Mini 2 RC</b> (also known as RC-N1, RCS231, WM161b-RC-N1, RCN1) as a controller for your favorite FPV drone simulator, you are in the right spot.

If you already have this controller you will be able to use it in the FPV SIM without the need to buy a new one, at least while you give it a test and decide if you like.

## Why I need this code?
Because DJI don't want you to use this controller this way. They might want you to buy a new one for this purpose.

## How does it work?
It works by reading and decoding the USB data, creating a new virtual controller, in this case a Dual Shock 4 virtual controller, and passing the inputs in real time from the <b>DJI Mini 2 RC</b> into the Dual Shock 4 virtual controller. Simple right?

## How can I run this code in my computer?

* First you'll need python installed in your computer, in this case Python 3.X.
You can download python from this link: https://www.python.org/downloads/windows/ and install it.

* Download the code and extract the zip file or if you know what you are doing you can also clone this repo.

![download-zip](https://github.com/ricardoneves93/DJIRemoteToFPVSimulator/assets/5951639/1a847bef-04c8-4f77-8333-cfb96ea1338a)

* Open you terminal and go to the directory where the zip file was extracted:
```
 cd Users\NevesFPV\Desktop\DJIRemoteToFPVSimulator
```

* Create a python virtual environment, a new folder called `venv` should be created:
```
python -m venv venv
```

* Activate the python virtual environment:
```
venv\Scripts\activate
```

* Install the dependecies:
```
pip install -r requirements.txt
```

* Run the python script
```
python main.py
```

* At this moment the script should be running and your terminal should look like this:

![terminal-1](https://github.com/ricardoneves93/DJIRemoteToFPVSimulator/assets/5951639/a588ed44-6de5-4f81-b427-d076dca93129)

* Turn on the <b>DJI Mini 2 RC</b> Remote and connect it by USB to your computer and press enter (A list of ports are going to appear)

![terminal-2](https://github.com/ricardoneves93/DJIRemoteToFPVSimulator/assets/5951639/14672a9c-aaf9-48a7-9ea5-74b8372c552a)

* It is hard to tell you what is the correct port. So choose one Port by typing the name of it, like `COM4` and press enter. It that is not the correct port, you'll get an error:

![terminal-3](https://github.com/ricardoneves93/DJIRemoteToFPVSimulator/assets/5951639/124b0311-62ee-45d8-920d-b6d27ea7ece1)

* If you see this error, run again the command `python main.py` and choose another port.

* When the correct port is chosen, you'll see something like this. If you move the axis, you'll see throttle, yaw, pitch and roll values to change between -1.0 and 1.0. <b>If you reach here it means that it is working correctly</b>:

![terminal-4](https://github.com/ricardoneves93/DJIRemoteToFPVSimulator/assets/5951639/94ef0eea-bcf0-4cd3-9d87-87f58457ea39)

* Open the FPV Simulator of your choice and it shoud detect it as a Playstation Dual Shock 4 controller. Calibrate the controller and you should be good to go!


This code was inspired in this repo https://github.com/usatenko/DjiMini2RCasJoystick, which unfortunately only works in linux.

If you like my work:
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/nevesfpv)

FPV simulators where I've tested:
* FPV Skydive
* Uncrashed
* FPV Freerider
* DRL (The Drone Racing League Simulator)
* TRYP






