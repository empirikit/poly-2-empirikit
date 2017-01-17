# poly-2-empirikit
Polymer 2 experiment (connecting to empiriKit board) utilizing WebUSB

Install prerequisites:

```
$ sudo npm install -g bower polymer-cli
$ bower install 
(choose the latest/preview versions of all conflicts)
```

Run:

```
$ polymer serve --port 8000 --open
(the current empiriKit board has localhost:8000 as trusted origin)
```

Linux:

Add the following udev rule to a file in /etc/udev/rules.d:

```
SUBSYSTEM=="usb", ATTRS{idVendor}=="1209", MODE:="0666", GROUP="plugdev"
```

Mac:
(untested but seems to connect - please report)

Windows:
Use Zadig to apply a libusb compatible WinUSB driver + WCID


In Chrome:

Enable the following flags:

chrome://flags/#enable-experimental-web-platform-features

chrome://flags/#enable-webusb

