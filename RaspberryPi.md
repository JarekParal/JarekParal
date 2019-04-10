# RaspberryPi

## Script for wlan_fi connecting

```sh
sudo cp wlan_fi_auth.sh /etc/network/if-up.d/
sudo chmod +X /etc/network/if-up.d/wlan_fi_auth.sh
ls -la /etc/network/

sudo cp wlan_fi_auth.sh /etc/cron.hourly/
sudo chmod +x /etc/cron.hourly/wlan_fi_auth.sh
ls -la /etc/cron.hourly/
```

