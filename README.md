# [Speedtestd](https://github.com/Edward-Knight/speedtestd)

_Simple internet speed monitoring_

Speedtestd is a small wrapper script around [speedtest-cli](https://github.com/sivel/speedtest-cli)
to continuously monitor internet speed.

The script is written in portable POSIX shell.
By default it performs a speed test every 30 minutes and logs to files in `/var/log`.
This can be changed by editing the variables at the top of the file.

A simple systemd unit file is provided for ease of installation.
After [installing speedtest-cli](https://github.com/sivel/speedtest-cli#installation)
and making `speedtest` available on the `${PATH}`, one can install and run speedtestd like so:

```shell script
cp speedtestd /usr/local/bin/speedtestd
cp speedtestd.service /etc/systemd/system/speedtestd.service
systemctl enable speedtestd
systemctl start speedtestd
```
