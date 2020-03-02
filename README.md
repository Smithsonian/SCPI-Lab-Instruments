SCPI Lab Instruments
====================

Communicate with various instruments in the receiver lab over Ethernet with SCPI commands.

Installation
------------

To install via ``pip``:

```bash
python3 -m pip install git+https://github.com/Smithsonian/SCPI-Lab-Instruments.git
```

To use the Keithley module, you also need to install the ``vxi11`` package. This can be installed by:

```bash
python3 -m pip install git+https://github.com/alexforencich/python-vxi11.git
```

Example
-------

```python
from labinstrument import *

# Connect to Hittite signal generator
sg = Hittite('192.168.0.159')
sg.set_power(-40, 'dBm')
sg.set_frequency(5, 'GHz')
sg.power_on()
```

References
----------

["System Power Supply Programming Using SCPI Commands"](https://www.keysight.com/us/en/assets/7018-06572/white-papers/5992-3841.pdf) from Keysight

