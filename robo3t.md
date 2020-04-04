# Install Robo3t On Ubuntu
Download the package form Robo3t site,and extract the package using the following command.

```bash
tar -xvzf robo3t-(...).tar.gz
```

Create a new floder in usr/local/bin

```bash
sudo mkdir /usr/local/bin/robo3t
```

Move the content of extracted directory to usr/local/bin

```bash
sudo mv  robo3t-.../* /usr/local/bin/robo3t
```

Change directory to cd /usr/local/bin/robo3t/bin, and give it permission using the following command.

```bash
sudo chmod +x robo3t ./robo3t
```

Download the icon for Robo3t using this link, [Robo3t icon](https://raw.githubusercontent.com/Studio3T/robomongo/master/src/robomongo/gui/resources/icons/logo-256x256.png), and save for example on /home with name "icon.png".

```bash
mv /home/icon.png /usr/local/bin/robo3t/bin
```

To make desktop icon for Robo3t, create a new file in usr/share/applications using the following command.

```bash
sudo vi /usr/share/applications/robo3t.desktop
```

Paste these in the robo3t.desktop file and save
```
[Desktop Entry]
Encoding=UTF-8
Type=Application
Name=Robo3t
Icon=/usr/local/bin/robo3t/bin/icon.png
Exec="/usr/local/bin/robo3t/bin/robo3t"
Comment=Robo3t 
Categories=Development;
Terminal=false
StartupNotify=true
Now, we can find the icon in application launcher menu by search for robo3t
```

### References
[Documentation](https://www.dotnetjalps.com/2018/03/install-robo3t-robmongo-ubuntu.html)
