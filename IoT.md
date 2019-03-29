# IoT

## [Hass.io - Home Assistant](https://www.home-assistant.io//)

You could use `Hass.io` as their own OS [`HassOs`](https://www.home-assistant.io/hassio/installation/) or use e.g. [`Hassbian`](https://www.home-assistant.io/docs/installation/hassbian/installation/) which is modified version of `Rasbian` with `Hass.io` services.

In comparison `Hass.io` you get with `Hassbian` these advantages:

- apt-get support
- probably full Raspbian support and compatibility

### Setting Wi-fi connection with `CONFIG` USB flash disk

If you setting connection on [Wi-fi through USB flash disk](https://github.com/home-assistant/hassos/blob/dev/Documentation/network.md) then the flash disk must have name `CONFIG`.

You don't need to care if the Wi-fi have WPA or WPA2 protection. Just put to config file `key-mgmt=wpa-psk`.

### How to check connection to Wi-fi on the device (RPi)

You can check if is the device available on your network with these application:
- [Advanced IP Scanner](http://www.advanced-ip-scanner.com) (Windows)
- [WiFiman](https://play.google.com/store/apps/details?id=com.ubnt.usurvey) (Android)

If you didn't find the `Hass.io` device (RPi) with this application, you can try command line on the device with monitor and keyboard:

#### Direct connection 

You need to connect the device to monitor through HDMI and plug-in USB keyboard. Then boot the device.

After login to `Hass.os` with default login `root` and empty passwords type this:

```bash
login # start the common Linux terminal without Hassio commands
nmcli # show the WLAN connection
```

## [EspHome](https://esphome.io)

EspHome is a platform for home devices base on ESP8266/ESP32 which communicate by MQTT protocol with soma server (e. g. `Hass.io`).

The configuration can be simply done with `.yaml` or programmed through `C++` API.

Support many devices (Sonnof), protocols (SPI, I2C...), sensors, displays, logic...
