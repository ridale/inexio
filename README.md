inexio
======

This is a kernel level driver for the inexio touch panels, and was tested on the 42" panel. These panels are usually overlayed onto a 42" LCD or Plasma screen.
This repo is imported from my original at http://repo.or.cz/w/inexio.git

There is a proper Kernel driver in the mainline kernel to handle the smaller 17" touchscreens and it should be preferred over this driver.

If you want to use this driver you would have to blacklist the other USB driver as Inexio used the same USB id for all of their devices.

The USB protocol was exactly the same as Inexio's original serial protocol and USB support was provided with an onboard serial to USB converter.

This is why this driver uses input attach to connect the /dev/ttyACM0 device to the evdev system.

Really you shouldn't have to use this code I am putting it up here as a historical record only.
