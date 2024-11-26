Introduction
============

CircuitPython helper library for the LSM6DSV family of motion sensors from ST.

Note that ST Electroncis makes several "LSM6DS" IMUs in their iNEMO line. However, they're not all 100% compatible. If you don't have on the following chips, you may need to use the `Adafruit_CircuitPython_LSM6DS library <https://github.com/adafruit/Adafruit_CircuitPython_LSM6DS>`_ instead. The code is this library is largely derived from that one, `in part to minimize library size <https://discord.com/channels/327254708534116352/327298996332658690/1307887971122413630>`_.

* LSM6DSV
* LSM6DSV16B
* LSM6DSV16BX
* LSM6DSV16X
* LSM6DSV32X

See the `ST iNEMO product page <https://www.st.com/en/mems-and-sensors/inemo-inertial-modules.html>`_ for more information.

A quick note on dev boards, I2C, and power
------------------------------------------

While writing this library, I used a `Sparkfun Micro 6DoF IMU Breakout - LSM6DSV16X (qwiic) <https://www.sparkfun.com/products/21336>`_ module for testing, connected to an Adafruit Hallowing M4 via it's STEMMA I2C port. This sort of worked, but when I went to test the gyroscope values, it was all over the place.

At first, I though this was due to something I'd missed in the driver. But the answer was simpler than that. Sparkfun's qwiic I2C interconnect assumes 3.3v to the port, and they design their breakouts with the assumption in mind. Adafruit's very similar STEMMA/STEMMA QT I2C port, however, is not concsistently 3.3v: it may also use 5v. This isn't normally a problem for STEMMA breakouts designed by Adafruit, since they typically set those boards up to transparently handle either voltage.

**So here's the tip: make sure that you're giving your dev module the voltage it expects ;-)**

Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_
* `Bus Device <https://github.com/adafruit/Adafruit_CircuitPython_BusDevice>`_
* `Register <https://github.com/adafruit/Adafruit_CircuitPython_Register>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://circuitpython.org/libraries>`_.

Installing from PyPI
=====================

This library is not yet available on PyPi.

Usage Example
=============

Usage examples are not yet available.

Documentation
=============

Documentation is not yet available.

Contributing
============

Contributions are welcome! Policy to come.
