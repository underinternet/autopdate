# autopdate
Auto Update is meant for Debian, Ubuntu and other similar linux OS.

# How To's
Simply copy and run in your terminal as root user:
```
wget -O /usr/share/autopdate https://raw.githubusercontent.com/ahrasis/autopdate/master/script
wget -O /etc/cron.d/autopdate https://raw.githubusercontent.com/ahrasis/autopdate/master/cron
chmod +x /usr/share/autopdate
```

# Time Setting
The time settings in the cron file is set to run at every hour at minute 40.

# Auto Reboot
The autopdate script reboot automatically if it finds /var/run/reboot-required exist.

# Log File
A log file will be created at /var/log/autopdate which may be disabled at your choice.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
