**[Deborphan](https://packages.debian.org/jessie/deborphan) finds "orphaned" packages on your system. It determines which packages have no other packages depending on their installation and shows you a list of these packages. It is most useful when finding libraries, but it can be used on packages in all sections.**
<br><br>

Install deborphan

`sudo apt update`
<br>
`sudo apt install deborphan`
<br><br>

Install aptitude

`sudo apt install aptitude`
<br><br>

Start of with a dry run to find out which packages we don't need

`deborphan --guess-all`
<br><br>

Remove unnecessary data packages

`sudo deborphan --guess-data | xargs sudo aptitude -y purge`
<br><br>

Delete unnecessary libraries

`sudo deborphan | xargs sudo apt-get -y remove --purge`
<br><br>

Run commands at least twice
