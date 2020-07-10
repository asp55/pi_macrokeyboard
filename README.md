# pi_macrokeyboard

#Setup the raspberry pi
Add the following line at the end of /boot/config.txt:

```bash
dtoverlay=dwc2
```

And the following two lines at the end of /etc/modules:

```bash
dwc2
libcomposite
```

#To Install
```bash
sudo cp pikeyboard_config.sh /usr/bin/pikeyboard_config.sh
sudo chmod +x /usr/bin/pikeyboard_config.sh
sudo cp pikeyboard.service /etc/systemd/system/pikeyboard.service
sudo chmod 644 /etc/systemd/system/pikeyboard.service
```

and finally, enable the service so that it starts on boot.
```bash
sudo systemctl enable pikeyboard
```