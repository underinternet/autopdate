# autopdate
This Auto Update script is meant for Debian, Ubuntu and other similar linux OS. Linux users that using unsimilar OS have to check what is the similar path to /var/run/reboot-required and change that accordingly.

# How To's
To automatically reboot immediately when required, simply copy and run in your terminal as root user:
```
rm -rf /usr/share/autopdate /etc/cron.d/autopdate
wget -O /usr/share/autopdate https://raw.githubusercontent.com/underinternet/autopdate/master/script --no-check-certificate
wget -O /etc/cron.d/autopdate https://raw.githubusercontent.com/underinternet/autopdate/master/cron --no-check-certificate
chmod +x /usr/share/autopdate
```

# Auto Reboot At Fixed Time?
If you want to auto reboot only at a fixed time like 3.30am, run the following command in your terminal:
```
sed -i "s/shutdown -r now/shutdown -r 3:30/" /usr/share/autopdate
```

# Cron Time Setting
The time settings in the cron file is set to run autopdate at every hour at minute 40, so do change it to suit your needs.

# Log File
A log file will be created at /var/log/autopdate which may be disabled at your choice by editing the cron file.

# License
Feel free to modify and fork, as though it is set to BSD3, none is mentioned in the script / cron file.
