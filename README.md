# Home Assistant udev rules

udev rules to grant Home Assistant access to certain devices, for example ZigBee dongles.

Expecting user group named `hass` to exist.

NOTE: Your device may be not supported yet, contributions welcome.

## Installation

```
cp 90-home-assistant-zigbee.rules /etc/udev/rules.d/
udevadm control --reload-rules
udevadm trigger
```

Should take effect immediately, no need to re-plug the device.

To verify ZigBee USB adapter ownership: `ls -la /dev/ttyUSB0*`
