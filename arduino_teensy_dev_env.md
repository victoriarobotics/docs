# Arduino-Teensy Development Environment
This document covers the steps to install the required development environment used by Team Victoria to develop
the Arduino-Teensy code used for the 2017 RoboMagellan robot.

These steps are not required to install the software that will run the robot, only for developing the Arduino-Teensy
code thar tuns the robot.

## Install Arduino IDE
For Teensy development, we are using the 1.6.12 version of the Arduino IDE.

* Download the 1.6.12 version (see https://www.arduino.cc/en/Main/OldSoftwareReleases#previous).
Make sure to download the "Linux Arm" version.
* Assuming the file was downloaded to ~/Downloads:
  * Open Terminal
  * `cd ~/Downloads`
  * `tar -xf arduino-1.6.12-linuxarm.tar.xz`
  * `cd ~`
  * `mv ~/Downloads/arduino-1.6.12/ ~/`
  * `cd arduino-1.6.12`
  * `sudo ./install.sh`

This will result in a directory installed at ~/arduino-1.6.12 and ~/Arduino. You can launch the Arduino IDE
from the system menu Applications->Programming->Arduino IDE.

## Install TeensyDuino
The microcontroller used for the 2017 RoboMagellan robot is the Teensy 3.5. Development for the Teensy
is performed in the Arduino IDE, but it requires for supporting libraries to be installed. Latest Teensy
information can be found [here](https://www.pjrc.com/teensy/teensyduino.html). These instructions are for
the TeensyDuino version 1.35.

* Download the TeensyDuino for ARM/Rasberry Pi (see https://www.pjrc.com/teensy/td_download.html).
Make sure to download the ARM/Rasberry Pi version.
* On https://www.pjrc.com/teensy/td_download.html, right click on "Linux udev rules" link and "Save link as..."
to ~/Downloads.
* Assuming all files were downloaded to ~/Downloads:
  * Open Terminal
  * `cd ~/Downloads`
  * The udev rule file gives non-root users permission to use the Teensy device.
    * `sudo cp 49-teensy.rules /etc/udev/rules.d/`
  * `chmod 755 TeensyduinoInstall.linuxarm`
  * `./TeensyduinoInstall.linuxarm`
  * The Teensyduino installer window will appear
    * First step: press "Next" button.
    * Second step: Navigate to the "/home/team-victoria/arduino-1.6.12" directory, press the "Next" button.
    The "Next" button will not be enabled until you navigate to the correct directory.
    * Third step: Choose "All" libraries, press the "Next" button.
    * Fourth step: Press the "Install" button.
    * Fifth step: After installation complete, press "Done".

## Install rosserial_arduino

## Install Pololu IMU and Mangetometer Libraries