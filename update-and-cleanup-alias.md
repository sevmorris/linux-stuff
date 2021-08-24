I created the file ~/.bash_aliases to add my aliases to, and added the following to ~/bashrc:

```
if [ -f ~/.bash_aliases ]; then
. ~/.bash_aliases
fi
```
<br><br>

Add the alias to ~/.bash_aliases:

`alias update='sudo apt update && sudo apt -o Dpkg::Options::="--force-confdef" dist-upgrade -y && sudo apt autoremove -y && if sudo test -f /var/run/reboot-required; then read -p "A reboot is required to finish installing updates. Press [ENTER] to reboot now, or [CTRL+C] to cancel and reboot later." && sudo reboot; else echo "A reboot is not required. Exiting..."; fi'`
