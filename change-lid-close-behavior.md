

`sudo nano /etc/systemd/logind.conf`
<br><br>

Change the following:

`#HandleLidSwitch=suspend`
<br>
to:

`HandleLidSwitch=ignore`
<br><br>

Apply the changes.
<br><br>

`sudo service systemd-logind restart`
<br><br>

Another option is to edit `/etc/UPower/UPower.conf` and change `IgnoreLid=` to `true`
