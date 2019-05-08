# update-linux
An easier way to update the linux distribution

# Notes
This gets you the latest bleeding edge kernel/firmware. There is always the possibility of regressions.

# Installing
```
sudo curl -L --output /usr/bin/update-linux https://raw.githubusercontent.com/gerlowski/update-linux/master/update-linux && sudo chmod +x /usr/bin/update-linux
```
# Usage
```
update-linux
```

You can check log output by typing:
```
cat /var/log/update-linux/update.log
```

# Contributing

Please fork this repository and contribute back using
[pull requests](https://github.com/Gerlowski/update-linux/pulls).

Any contributions, large or small, major features, bug fixes, are welcomed and appreciated
but will be thoroughly reviewed.

# Troubleshooting
There are two possible problems related to SSL certificates that may prevent this tool from working.
- The time may be set incorrectly on your linux, which you can fix by setting the time using NTP.
```
sudo apt-get install ntpdate
sudo ntpdate -u ntp.ubuntu.com
```

- The other possible issue is that you might not have the ```ca-certificates``` package installed, and so GitHub's SSL certificate isn't trusted. If you are on Debian, you can resolve this by typing:
```
sudo apt-get install ca-certificates
```
