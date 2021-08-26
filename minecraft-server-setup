Update the apt sources lists: `sudo apt update`

Install any available updates of the packages already installed: `sudo apt upgrade -y`

Install these packages: `sudo apt install gnupg curl dirmngr nano unzip netatalk screen avahi-daemon -y`

Add the repository needed to install Java:

> **For Debian** Use the command `sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 73C3DB2A` to add the key needed for the Java repository.

> Add the repository by executing the command `echo "deb http://ppa.launchpad.net/linuxuprising/java/ubuntu focal main" | tee /etc/apt/sources.list.d/java.list`
<br><br>

> **For Ubuntu** install the package for managing repositories using the following command: `sudo apt install software-properties-common -y`

Update the apt sources lists again: `sudo apt update`

Install Java: `sudo apt install oracle-java16-installer -y` and follow the prompts.

Add a user named **minecraft** who will run the Minecraft Server: `sudo adduser --disabled-login minecraft`

Give **minecraft** a password: `sudo passwd minecraft`, and switch to user: `su minecraft`

Go to the home directory: `cd`

Enter the command `wget https://download.getbukkit.org/spigot/spigot-1.17.jar` to download the (current) latest version of Spigot.

Use `la` to see the downloaded jar file.

Create a start script: `nano start.sh`

- Copy/paste: `screen -AmdS minecraft java -Xms4096M -Xmx4096M -jar /home/minecraft/spigot-1.17.jar nogui` into the document.

Save & exit (**ctrl + x then y**)

Create a stop script: `nano stop.sh`

- Copy/paste `screen -r minecraft -X quit` into the document.

Save & exit

Make the scripts executable: `chmod +x start.sh stop.sh`

In order to be able to start the Minecraft server, you must first accept the license terms. To do this, execute the command `echo "eula = true" > eula.txt`. This creates a new file which indicates that you accepted these license terms.

Start the server: `./start.sh`

Open the Minecraft server console: `screen -r minecraft`

To exit the console press **ctrl + a then d**
