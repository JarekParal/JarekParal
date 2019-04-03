# Windows Subsystem for Linux (WSL)

## Ubuntu

### [avahi](https://wiki.archlinux.org/index.php/avahi)
"Avahi is a free Zero-configuration networking (zeroconf) implementation, including a system for multicast DNS/DNS-SD service discovery."

#### How to looking for devices with `avahi`:

```bash
sudo apt-get install avahi-utils
sudo service dbus start
sudo service avahi-daemon start
avahi-browse -atr # show all devices with avahi
```
