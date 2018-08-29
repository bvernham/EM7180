<a href="https://www.tindie.com/products/onehorse/ultimate-sensor-fusion-solution/"><img src="sentral.jpg" width=300></a>

This repository contains Arduino, Raspberry Pi (WiringPi), and Linux i2cdev
libraries and examples for working with the incredible <a
href="https://www.tindie.com/products/onehorse/ultimate-sensor-fusion-solution/">
EM7180 Ultimate Sensor Fusion Solution</a> from Pesky Products. 

To use this library you will also need our cross-platform support 
[library](https://github.com/simondlevy/CrossPlatformDataBus).

We have tested this EM7180 library on the following hardware:

* Ladybug STM32L4 board from Tlera Corp

* Teensy 3.2, 3.6

* Raspberry Pi 3

* NVIDIA Jetson TX1

The library provides two C++ classes for working with the EM7180 SENtral sensor hub on this board:

* An <b>EM7180</b> class providing a convenient API for the full functionality of the EM7180 unit

* An <b>EM7180_Master</b> class that runs the EM7180 in master mode, for simple access to the sensor-fusion features

The <b>examples</b> directory contains sketches showing how to use these two classes. As usual, just clone the repo
into your Arduino libraries folder to get started. The class library and
examples were adapted from Kris Winer's [repository](https://github.com/kriswiner/EM7180_SENtral_sensor_hub).
We strongly recommend reading Kris's  [wiki](https://github.com/kriswiner/EM7180_SENtral_sensor_hub/wiki) for
a comprehensive overview of the EM7180 and other sensor-fusion solutions.

RaspberryPi users should download and install [WiringPi](http://wiringpi.com/),
then cd to <b>EM7180/extras/wiringpi</b>, and run <b>make</b>
to build the examples.  You may have to run the examples as root; e.g., <tt>sudo ./GetInfo</tt>.

Users of NVIDIA Jetson and other Linux-based boards should install I<sup>2</sup>C support by running the command:
<pre>
  sudo apt-get install libi2c-dev i2c-tools
</pre>
You can then can cd to <b>EM7180/extras/i2cdev</b>, and run
<b>make</b>. You may have to run the examples as root; e.g., <tt>sudo ./GetInfo</tt>.

An asynchronous [version](https://github.com/bmegli/EM7180.git) of this library is also available for Teensy 3.5.

