Backup the configuration file.

`sudo cp -n /etc/default/grub /etc/default/grub.backup`
<br><br>

Edit the configuration file.

`sudo nano /etc/default/grub`
<br><br>

Comment out:

`GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"`
<br><br>

Set GRUB_CMDLINE_LINUX to:

`GRUB_CMDLINE_LINUX="text"`
<br><br>

Uncomment:

`GRUB_TERMINAL="console"`
<br><br>

Save the file and apply changes.

`sudo update-grub`
<br><br>

And finally:

`sudo systemctl set-default multi-user.target`
