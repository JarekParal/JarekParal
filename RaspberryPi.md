# RaspberryPi

## Script for wlan_fi connecting

```sh
sudo cp wlan_fi_auth.sh /etc/network/if-up.d/wlan_fi_auth
sudo chmod +X /etc/network/if-up.d/wlan_fi_auth.sh
ls -la /etc/network/

sudo cp wlan_fi_auth /etc/cron.hourly/
sudo chmod +x /etc/cron.hourly/wlan_fi_auth
ls -la /etc/cron.hourly/
```

Check if the [script run after `if-up`](https://stackoverflow.com/a/45292665)

```sh
sudo ifup --all -v
```
