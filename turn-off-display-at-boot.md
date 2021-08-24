I had to do this with my MacBook Air running Ubuntu in console mode.

Edit the crontab file. The crontab file is a daemon that performs user-edited tasks at specific times and events.

`sudo crontab -e`
<br><br>

Add the following to execute at boot:

`@reboot sudo bash -c "echo 0 > /sys/class/backlight/intel_backlight/brightness;"`
