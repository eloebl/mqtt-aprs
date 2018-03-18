# mqtt-aprs
Connects to the specified APRS-IS server, and posts the APRS output to MQTT.  Can parse parameters, or dump the raw JSON from aprslib.  It's currently for receive only from APRS-IS and sending to an MQTT server.

This script uses the aprslib, https://github.com/rossengeorgiev/aprs-python, to do the heavy APRS lifting.

INSTALL
=================
```
sudo apt-get install git python-pip

sudo pip install setuptools
sudo pip install setproctitle
sudo pip install paho-mqtt
sudo pip install aprslib

mkdir /etc/mqtt-aprs/
git clone git://github.com/mloebl/mqtt-mqtt-aprs.git /usr/local/mqtt-aprs/
cp /usr/local/mqtt-aprs/mqtt-aprs.cfg.example /etc/mqtt-aprs/mqtt-aprs.cfg
cp /usr/local/mqtt-aprs/mqtt-aprs.init /etc/init.d/mqtt-aprs
pdate-rc.d mqtt-aprs defaults
cp /usr/local/mqtt-aprsp/mqtt-aprs.default /etc/default/mqtt-aprs
```
Edit /etc/default/mqtt-aprs and /etc/mqtt-aprs/mqtt-aprs.cfg to suit:

`/etc/init.d/mqtt-aprs start`

APRS is a registered trademark Bob Bruninga, WB4APR
