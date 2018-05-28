# autopdate
Auto Update is meant for Debian, Ubuntu and other similar linux OS. DO NOT MIX Auto Reboot When Required with Auto Reboot At Fixed Time as their approaches are different. Use the one that you prefer only.

# Auto Reboot When Required
This autopdate script reboot automatically if it finds /var/run/reboot-required exist.

# Auto Reboot At Fixed Time
This autopdate script2 reboot at a fixed time if it finds /var/run/reboot-required exist.

# How To's (Auto Reboot When Required)
To automatically reboot immediately when required, simply copy and run in your terminal as root user:
```
rm -rf /usr/share/autopdate /etc/cron.d/autopdate
wget -O /usr/share/autopdate/autopdate https://raw.githubusercontent.com/ahrasis/autopdate/master/script --no-check-certificate
wget -O /etc/cron.d/autopdate https://raw.githubusercontent.com/ahrasis/autopdate/master/cron --no-check-certificate
chmod +x /usr/share/autopdate/autopdate
```

# How To's (Auto Reboot At Fixed Time)
To automatically reboot only at a fixed time, simply copy and run in your terminal as root user:
```
rm -rf /usr/share/autopdate /etc/cron.d/autopdate
mkdir /usr/share/autopdate && cd /usr/share/autopdate
wget https://raw.githubusercontent.com/ahrasis/autopdate/master/script2 --no-check-certificate
wget https://raw.githubusercontent.com/ahrasis/autopdate/master/cron --no-check-certificate
wget https://raw.githubusercontent.com/ahrasis/autopdate/master/cron2 --no-check-certificate
chmod +x /usr/share/autopdate/autopdate
```

# Cron Time Setting
The time settings in the cron file is set to run autopdate at every hour at minute 40. The time to reboot is at 3.30 am if fixed time is used. Change them to suit your needs.

# Log File
A log file will be created at /var/log/autopdate which may be disabled at your choice.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
