# smart-cooler
Smcooler system servis to control the fan on raspberry
---
smcooler - python script<br>
smcooler.service - configuration file of service<br>
Schematic_Smart-cooler.zip - electrical schematics<br>

### How to download the project:<br>
    # cd existing_folder
    # git init
    # git remote add origin git://github.com/belov-ve/smart-cooler
    # git pull origin master

### How to install and activate the service:<br>
    # apt-get install python-rpi.gpio python3-rpi.gpio
    # chmod +x smcooler
    # cp smcooler /usr/bin/
    # cp smcooler.service /etc/systemd/system/
    # systemctl enable smcooler.service

### How to check the script and service after installation:<br>
    # smcooler
    or
    # systemctl status smcooler.service

### Service commands:<br>
    # systemctl start smcooler
    # systemctl stop smcooler
    # systemctl restart smcooler

### How to get the temperature of the raspberry processor:<br>
    # smcooler
    (to interrupt press CTRL + C)
    
